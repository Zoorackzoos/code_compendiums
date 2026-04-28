# **.mbx (Astro Starlight) Compendium**

## **1\. File Structure Basics**

\---  
title: Page title  
\---

// Imports (JS/TS-style)  
import {Component} from "@astrojs/starlight/components";  
import CustomComponent from "../components/CustomComponent.astro";

// Content starts here  
Your text goes here.

* Frontmatter (between `---`) defines metadata like `title`.  
* After frontmatter, you can use Markdown \+ JSX-like components.

---

## **2\. Markdown Basics (Supported)**

\# Heading 1  
\#\# Heading 2  
\#\#\# Heading 3

Paragraph text.

\- Bullet list  
\- Another item

1\. Numbered list  
1\. Another step

\*\*Bold\*\*  
\*Italic\*  
\[Link text\](/help/example)

---

## **3\. Importing Components**

import {Tabs, TabItem} from "@astrojs/starlight/components";  
import MyComponent from "../components/MyComponent.astro";

* You must import components before using them.  
* Paths are relative.

---

## **4\. Using Components**

\<MyComponent\>  
  Content inside component  
\</MyComponent\>

Self-closing:

\<MyComponent /\>

---

## **5\. Tabs UI Pattern**

\<Tabs\>  
  \<TabItem label="Desktop"\>  
    Desktop content  
  \</TabItem\>

  \<TabItem label="Mobile"\>  
    Mobile content  
  \</TabItem\>  
\</Tabs\>

---

## **6\. Step-by-Step Instructions**

\<FlattenedSteps\>  
  1\. Step one  
  1\. Step two  
  1\. Step three  
\</FlattenedSteps\>

* Always use `1.` for each step (auto-numbering).

---

## **7\. Reusable Includes**

import MessageActions from "../include/\_MessageActions.mdx";

\<MessageActions /\>

* Used for shared UI snippets.

---

## **8\. Admonitions / Tips**

\<ZulipTip\>  
  Helpful tip text here.  
\</ZulipTip\>

---

## **9\. Icons**

import EditIcon from "\~icons/zulip-icon/edit";

Click the icon \<EditIcon /\>

---

## **10\. Linking to Other Docs**

\[Edit a message\](/help/edit-a-message)

* Use absolute paths starting with `/help/`.

---

## **11\. Combining Markdown \+ Components**

Click the \*\*edit\*\* button \<EditIcon /\> to continue.

---

## **12\. Conditional Content via Tabs (Common Pattern)**

\<Tabs\>  
  \<TabItem label="Web/Desktop"\>  
    \<FlattenedSteps\>  
      1\. Click something  
      1\. Do thing  
    \</FlattenedSteps\>  
  \</TabItem\>

  \<TabItem label="Mobile"\>  
    \<FlattenedSteps\>  
      1\. Tap something  
      1\. Do thing  
    \</FlattenedSteps\>  
  \</TabItem\>  
\</Tabs\>

---

## **13\. Sections**

\#\# Section Title

Content here

---

## **14\. Related Articles Section**

\#\# Related articles

\* \[Article one\](/help/article-one)  
\* \[Article two\](/help/article-two)

---

## **15\. Best Practices**

* Keep sentences short and instructional.  
* Use **bold** for UI labels.  
* Use components for structure (Tabs, Steps, Tips).  
* Reuse includes whenever possible.  
* Keep consistent wording (Click vs Tap).

---

## **16\. Common Pattern Template**

\---  
title: Your feature  
\---

import {Tabs, TabItem} from "@astrojs/starlight/components";  
import FlattenedSteps from "../../components/FlattenedSteps.astro";  
import ZulipTip from "../../components/ZulipTip.astro";

Intro paragraph explaining feature.

\<ZulipTip\>  
  Optional helpful tip.  
\</ZulipTip\>

\#\# Do the thing

\<Tabs\>  
  \<TabItem label="Desktop/Web"\>  
    \<FlattenedSteps\>  
      1\. Step  
      1\. Step  
    \</FlattenedSteps\>  
  \</TabItem\>

  \<TabItem label="Mobile"\>  
    \<FlattenedSteps\>  
      1\. Step  
      1\. Step  
    \</FlattenedSteps\>  
  \</TabItem\>  
\</Tabs\>

\#\# Related articles

\* \[Something\](/help/something)

---

## **17\. Mental Model**

Think of `.mbx` as:

* Markdown  
  * React-style components  
  * Astro imports

You are writing docs that are both:

* readable text  
* structured UI

---

## **18\. Common Mistakes**

* Forgetting to import components  
* Using normal numbering instead of `1.`  
* Incorrect relative paths  
* Not closing components properly

---

This document is your quick-reference for writing Zulip help center pages in `.mbx`. Keep it open while you work 👍

