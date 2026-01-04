# starlight-md2html

**Description**
starlight-md2html is a utility module that converts standard Markdown (.md) files into fully structured, ready-to-use HTML files.
It is designed for developers who want fast Markdown publishing without manually writing HTML.




## Why starlight-md2html?

 - Converts Markdown into clean HTML - Includes full HTML document structure - Built-in styling for readability - Supports tables, code blocks, lists, headings, and links - Works perfectly with starlight-mdconverter  


## Installation

` npm install marked ` 


## Core Functions

**convertMDToHTML(mdContent)**
Converts Markdown text into HTML content.

 - **mdContent** – Markdown content as a string - Returns parsed HTML body  


**convertFile(inputFilePath, outputFilePath)**
Converts a Markdown file into a complete HTML file.

 - **inputFilePath** – Path to the .md file - **outputFilePath** – Path to save the .html file - Automatically wraps content in a full HTML layout  


## Supported Markdown Features

 - Headings (#, ##, ###) - Bold and italic text - Inline and block code - Tables - Ordered and unordered lists - Links and images - Blockquotes  


## Workflow Example

 - Write documentation in **.slmd** - Convert to **.md** using starlight-mdconverter - Convert **.md** to **.html** using starlight-md2html  


## Advantages

 - No manual HTML writing - Consistent layout and styling - Easy publishing to web or docs sites - Ideal for documentation, blogs, and guides  


## Who Should Use This?

 - Library authors - Documentation writers - CLI tool developers - Static site generators  


## Conclusion

starlight-md2html completes the Starlight documentation pipeline by transforming Markdown into polished HTML.
Combined with SLMD, it enables a fast, readable, and developer-friendly documentation workflow.
