# XML code compendium

# **1\. XML Declaration**

## **Purpose**

Specifies the XML version and encoding used in the document.

## **Example**

\<?xml version="1.0" encoding="UTF-8"?\>

# **2\. Root Element**

## **Purpose**

Defines the single top-level container for all XML data.

## **Example**

\<note\>  
  \<to\>User\</to\>  
  \<from\>Assistant\</from\>  
\</note\>

# **3\. Elements**

## **Purpose**

Represents structured data using opening and closing tags.

## **Example**

\<message\>Hello World\</message\>

# **4\. Attributes**

## **Purpose**

Provides additional information about elements.

## **Example**

\<user id="123" role="admin"\>John\</user\>

# **5\. Nested Elements**

## **Purpose**

Allows elements to be placed inside other elements to create hierarchy.

## **Example**

\<book\>  
  \<title\>XML Guide\</title\>  
  \<author\>Jane Doe\</author\>  
\</book\>

# **6\. Self-Closing Tags**

## **Purpose**

Represents empty elements without separate closing tags.

## **Example**

\<br /\>  
\<image src="pic.png" /\>

# **7\. Comments**

## **Purpose**

Adds notes that are ignored by the XML parser.

## **Example**

\<\!-- This is a comment \--\>

# **8\. CDATA Section**

## **Purpose**

Allows inclusion of text that should not be parsed as XML.

## **Example**

\<\!\[CDATA\[  
\<notATag\>This won't be parsed\</notATag\>  
\]\]\>

# **9\. Entities**

## **Purpose**

Represents reserved characters using predefined codes.

## **Example**

\&lt;tag\&gt; \&amp; \&quot;text\&quot;

# **10\. Namespaces**

## **Purpose**

Avoids element name conflicts by qualifying names.

## **Example**

\<root xmlns:h="http://www.w3.org/TR/html4/"\>  
  \<h:table\>  
    \<h:tr\>  
      \<h:td\>Data\</h:td\>  
    \</h:tr\>  
  \</h:table\>  
\</root\>

# **11\. Processing Instructions**

## **Purpose**

Provides instructions to applications processing the XML.

## **Example**

\<?xml-stylesheet type="text/xsl" href="style.xsl"?\>

# **12\. DTD Declaration**

## **Purpose**

Defines the structure and legal elements of an XML document.

## **Example**

\<\!DOCTYPE note \[  
  \<\!ELEMENT note (to,from)\>  
  \<\!ELEMENT to (\#PCDATA)\>  
  \<\!ELEMENT from (\#PCDATA)\>  
\]\>

# **13\. XML Schema Reference**

## **Purpose**

Links XML to an external schema for validation.

## **Example**

\<note xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  
      xsi:noNamespaceSchemaLocation="note.xsd"\>  
\</note\>

# **14\. Text Content**

## **Purpose**

Stores raw text inside elements.

## **Example**

\<greeting\>Hello, user\!\</greeting\>

# **15\. Lists via Repeated Elements**

## **Purpose**

Represents collections using repeated tags.

## **Example**

\<items\>  
  \<item\>One\</item\>  
  \<item\>Two\</item\>  
  \<item\>Three\</item\>  
\</items\>

# **16\. Attributes vs Elements**

## **Purpose**

Shows two ways to represent data.

## **Example**

\<user id="1"\>John\</user\>  
\<user\>  
  \<id\>1\</id\>  
  \<name\>John\</name\>  
\</user\>

# **17\. Whitespace Handling**

## **Purpose**

Controls how whitespace is interpreted.

## **Example**

\<text xml:space="preserve"\>   spaced text   \</text\>

# **18\. Encoding Special Characters**

## **Purpose**

Ensures reserved characters are properly displayed.

## **Example**

\&lt; \&gt; \&amp; \&apos; \&quot;

# **19\. XML Declaration with Standalone**

## **Purpose**

Indicates whether the document relies on external markup declarations.

## **Example**

\<?xml version="1.0" encoding="UTF-8" standalone="yes"?\>

# **20\. Simple XML Document Example**

## **Purpose**

Demonstrates a complete XML structure.

## **Example**

\<?xml version="1.0" encoding="UTF-8"?\>  
\<library\>  
  \<book id="1"\>  
    \<title\>Learn XML\</title\>  
    \<author\>Jane Doe\</author\>  
  \</book\>  
\</library\>

# **21\. Well-Formed Document Rules**

## **Purpose**

Ensures XML follows strict syntax rules.

## **Example**

\<\!-- Must have one root, properly nested tags \--\>  
\<root\>  
  \<a\>  
    \<b\>\</b\>  
  \</a\>  
\</root\>

# **22\. Case Sensitivity**

## **Purpose**

Shows that XML tags are case-sensitive.

## **Example**

\<Item\>Wrong\</Item\>  
\<item\>Correct\</item\>

# **23\. Proper Nesting**

## **Purpose**

Requires tags to be correctly nested.

## **Example**

\<\!-- Incorrect \--\>  
\<a\>\<b\>\</a\>\</b\>

\<\!-- Correct \--\>  
\<a\>\<b\>\</b\>\</a\>

# **24\. Required Closing Tags**

## **Purpose**

Ensures all non-empty elements are closed.

## **Example**

\<tag\>\</tag\>

# **25\. Attribute Quoting**

## **Purpose**

Requires attribute values to be quoted.

## **Example**

\<user name="Alice" /\>

# **26\. Multiple Attributes**

## **Purpose**

Allows multiple attributes in one element.

## **Example**

\<car make="Toyota" model="Camry" year="2022" /\>

# **27\. Default Namespace**

## **Purpose**

Defines a namespace without a prefix.

## **Example**

\<root xmlns="http://example.com"\>  
  \<child\>Data\</child\>  
\</root\>

# **28\. Prefixed Namespace**

## **Purpose**

Uses prefixes to distinguish elements.

## **Example**

\<x:tag xmlns:x="http://example.com"\>Value\</x:tag\>

# **29\. Mixed Content**

## **Purpose**

Allows text and elements together.

## **Example**

\<p\>This is \<b\>bold\</b\> text.\</p\>

# **30\. Empty Element Expansion**

## **Purpose**

Shows equivalence of self-closing and expanded tags.

## **Example**

\<tag /\>  
\<tag\>\</tag\>

# **31\. ID Attribute (DTD)**

## **Purpose**

Defines a unique identifier for elements.

## **Example**

\<\!ATTLIST user id ID \#REQUIRED\>

# **32\. IDREF Attribute**

## **Purpose**

References another element by ID.

## **Example**

\<\!ATTLIST order userID IDREF \#REQUIRED\>

# **33\. Required Attribute (DTD)**

## **Purpose**

Specifies that an attribute must be present.

## **Example**

\<\!ATTLIST user name CDATA \#REQUIRED\>

# **34\. Optional Attribute (DTD)**

## **Purpose**

Defines optional attributes.

## **Example**

\<\!ATTLIST user age CDATA \#IMPLIED\>

# **35\. Default Attribute Value**

## **Purpose**

Provides a default value for an attribute.

## **Example**

\<\!ATTLIST user role CDATA "guest"\>

# **36\. Element Order (DTD)**

## **Purpose**

Specifies required child element order.

## **Example**

\<\!ELEMENT person (name, age)\>

# **37\. Choice in DTD**

## **Purpose**

Allows one of several elements.

## **Example**

\<\!ELEMENT contact (email | phone)\>

# **38\. Repetition in DTD**

## **Purpose**

Allows multiple occurrences of elements.

## **Example**

\<\!ELEMENT items (item\*)\>

# **39\. One or More (+)**

## **Purpose**

Requires at least one occurrence.

## **Example**

\<\!ELEMENT items (item+)\>

# **40\. Optional Element (?)**

## **Purpose**

Makes an element optional.

## **Example**

\<\!ELEMENT middleName (\#PCDATA)?\>

# **41\. XPath Basic Path**

## **Purpose**

Selects nodes using path expressions.

## **Example**

/bookstore/book/title

# **42\. XPath Attribute Selection**

## **Purpose**

Selects attributes in XPath.

## **Example**

//book/@id

# **43\. XPath Wildcard**

## **Purpose**

Selects any element.

## **Example**

//\*/title

# **44\. XPath Predicate**

## **Purpose**

Filters nodes based on conditions.

## **Example**

//book\[price\>30\]

# **45\. XPath Indexing**

## **Purpose**

Selects elements by position.

## **Example**

//book\[1\]

# **46\. XSLT Transformation**

## **Purpose**

Transforms XML into other formats.

## **Example**

\<xsl:template match="/"\>  
  \<html\>\<body\>\<h1\>Data\</h1\>\</body\>\</html\>  
\</xsl:template\>

# **47\. XSLT Value Extraction**

## **Purpose**

Extracts values in XSLT.

## **Example**

\<xsl:value-of select="title" /\>

# **48\. XML Validation Concept**

## **Purpose**

Checks XML against DTD or Schema.

## **Example**

\<\!-- Validated against .xsd or .dtd \--\>

# **49\. JSON vs XML Representation**

## **Purpose**

Compares XML structure to JSON.

## **Example**

\<name\>John\</name\>

# **50\. Complex XML Example**

## **Purpose**

Shows a more advanced structured document.

## **Example**

\<store\>  
  \<product id="101"\>  
    \<name\>Laptop\</name\>  
    \<price\>999.99\</price\>  
    \<specs\>  
      \<ram\>16GB\</ram\>  
      \<cpu\>Intel i7\</cpu\>  
    \</specs\>  
  \</product\>  
\</store\>

