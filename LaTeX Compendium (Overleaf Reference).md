# **LaTeX Compendium (Overleaf Reference)**

## **1\. Basic Document Structure**

\\documentclass{article}

\\usepackage\[utf8\]{inputenc}  
\\usepackage{amsmath, amssymb}  
\\usepackage{graphicx}  
\\usepackage{hyperref}

\\title{Your Title}  
\\author{Your Name}  
\\date{\\today}

\\begin{document}

\\maketitle

\\section{Introduction}  
Hello world\!

\\end{document}

---

## **2\. Sections & Organization**

\\section{Section}  
\\subsection{Subsection}  
\\subsubsection{Subsubsection}  
\\paragraph{Paragraph}

Table of contents:

\\tableofcontents

---

## **3\. Text Formatting**

\\textbf{Bold}  
\\textit{Italic}  
\\underline{Underline}  
\\texttt{Monospace}  
\\emph{Emphasis}

---

## **4\. Math Mode**

### **Inline Math**

$ a^2 \+ b^2 \= c^2 $

### **Display Math**

\\\[ a^2 \+ b^2 \= c^2 \\\]

### **Equation Environment**

\\begin{equation}  
E \= mc^2  
\\end{equation}

Unnumbered:

\\begin{equation\*}  
E \= mc^2  
\\end{equation\*}

---

## **5\. Common Math Symbols**

\\alpha \\beta \\gamma \\delta  
\\pi \\theta \\lambda

\\sum \\int \\infty  
\\approx \\neq \\leq \\geq

---

## **6\. Fractions, Powers, Roots**

\\frac{a}{b}  
x^2  
\\sqrt{x}  
\\sqrt\[n\]{x}

---

## **7\. Brackets & Sizing**

\\left( \\frac{a}{b} \\right)  
\\left\[ x^2 \\right\]  
\\left\\{ x \\right\\}

---

## **8\. Matrices & Linear Algebra**

\\begin{bmatrix}  
a & b \\\\  
c & d  
\\end{bmatrix}

Augmented matrix:

\\begin{bmatrix}  
1 & 2 & | & 3 \\\\  
0 & 1 & | & 4  
\\end{bmatrix}

Other types:

pmatrix  % ()  
vmatrix  % determinant

Vectors:

\\vec{v}  
\\mathbf{v}

---

## **9\. Aligning Equations**

\\begin{align}  
a &= b \+ c \\\\  
d &= e \+ f  
\\end{align}

No numbering:

\\begin{align\*}  
...  
\\end{align\*}

---

## **10\. Cases / Piecewise Functions**

\\begin{cases}  
x^2 & x \> 0 \\\\  
0 & x \\leq 0  
\\end{cases}

---

## **11\. Systems of Equations**

\\begin{cases}  
x \+ y \= 1 \\\\  
2x \- y \= 3  
\\end{cases}

---

## **12\. Lists**

### **Itemized**

\\begin{itemize}  
  \\item Item 1  
  \\item Item 2  
\\end{itemize}

### **Enumerated**

\\begin{enumerate}  
  \\item First  
  \\item Second  
\\end{enumerate}

---

## **13\. Tables (Advanced)**

\\usepackage{booktabs}

\\begin{tabular}{cc}  
\\toprule  
A & B \\\\  
\\midrule  
1 & 2 \\\\  
\\bottomrule  
\\end{tabular}

---

## **14\. Images**

\\begin{figure}\[h\]  
  \\centering  
  \\includegraphics\[width=0.5\\textwidth\]{image.png}  
  \\caption{Your caption}  
  \\label{fig:example}  
\\end{figure}

---

## **15\. References & Labels**

\\label{sec:intro}  
\\ref{sec:intro}

---

## **16\. Hyperlinks**

\\href{https://example.com}{Link text}

---

## **17\. Comments**

% This is a comment

---

## **18\. Useful Packages**

\\usepackage{amsmath}  
\\usepackage{amssymb}  
\\usepackage{graphicx}  
\\usepackage{hyperref}  
\\usepackage{geometry}  
\\usepackage{xcolor}  
\\usepackage{fancyhdr}  
\\usepackage{booktabs}

---

## **19\. Page Layout & Headers**

\\usepackage\[margin=1in\]{geometry}

\\usepackage{fancyhdr}  
\\pagestyle{fancy}  
\\fancyhead\[L\]{Left}  
\\fancyhead\[R\]{Right}

---

## **20\. Code Blocks (Better)**

\\usepackage{listings}

\\begin{lstlisting}  
int main() {  
  return 0;  
}  
\\end{lstlisting}

---

## **21\. Custom Commands**

\\newcommand{\\R}{\\mathbb{R}}  
\\newcommand{\\vecb}\[1\]{\\mathbf{\#1}}

---

## **22\. Math Tricks**

Text in math:

\\text{if } x \> 0

Operators:

\\sin \\cos \\log \\ln

Limits:

\\lim\_{x \\to \\infty}

---

## **23\. Spacing**

a\\,b   % small space  
a\\quad b  
a\\qquad b

---

## **24\. Theorem Environments**

\\usepackage{amsthm}

\\newtheorem{theorem}{Theorem}

\\begin{theorem}  
Statement here  
\\end{theorem}

---

## **25\. Colors**

\\usepackage{xcolor}

\\textcolor{red}{Hello}

---

## **26\. Footnotes**

Hello\\footnote{This is a footnote}

---

## **27\. Bibliography (Basic)**

\\begin{thebibliography}{9}  
\\bibitem{ref1} Author, Title  
\\end{thebibliography}

---

## **28\. Common Errors & Fixes**

* Missing `$` → math won’t compile  
* Forgetting `\end{}` → crash  
* Extra `&` → alignment error  
* File not found → check path

---

## **29\. Debugging Strategy**

1. Comment out sections  
2. Recompile  
3. Narrow error  
4. Fix syntax

---

## **30\. Minimal Template**

\\documentclass{article}  
\\usepackage{amsmath, amssymb, graphicx}

\\begin{document}

Your content here.

\\end{document}

## **31\. New page**

\\newpage

---

End of Compendium

