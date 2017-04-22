---
layout: post
title:  "XML Document Schema Definition"
categories: jekyll update
---
### Question:
Fully explain what DTD (Document Type Definition) or XML Schema is and its function in defining and verifying the validity of XML documents.

<hr>


DTD's(Document Type Definition) give everyone the same blocks to work with when writing XML so that there are no differences between two parties and the validity of the documents are maintained.


There are two ways to use a DTD: external or internal.  As the names apply an external DTD uses a file that is outside the document where as the internal DTD is setup in the same files as where the XML is written. 

An eternal DTD can link to files in several ways: 

* **Public DTD** 

Identified by the keyword `PUBLIC`. Is intended for broad use. 

```xml
<!DOCTYPE root_element PUBLIC "DTD_name" "DTD_location">
```

* **Private DTD**

Private DTD's are identified by the keyword `SYSTEM` and allow for a single author or multiple authors. 

```xml
<!DOCTYPE root_element SYSTEM "DTD_location">
```


An internal DTD we would set up in the document itself. We start with doctype like this at the top of the document and add declarations in the middle.

```xml
<!DOCTYPE books SYSTEM "books.dtd" [
    <!-- additional DTD declarations here... -->
]>
```


A completed version would look like this as an example : 

```xml
<?xml version="1.0"?>
<!DOCTYPE files [
<!ELEMENT files (file+)>
<!ELEMENT file (title,artist+,album?,genre?)>
<!ELEMENT title (#PCDATA)>
<!ELEMENT artist (#PCDATA)>
<!ELEMENT album (#PCDATA)>
<!ELEMENT genre (#PCDATA)>
<!ATTLIST file id CDATA #REQUIRED>
<!ATTLIST file trklength CDATA #REQUIRED>
]>
```



