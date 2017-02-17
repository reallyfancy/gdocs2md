gdocs2md
========

A simple Google Apps script to convert a properly formatted Google Drive Document to the markdown (.md) format. This is a customised version to suit my workflow, based on [the original by Renato Mangini](https://github.com/mangini/gdocs2md).

## How to use

  * Adding this script to your document:
    * Open your Google Drive document (http://drive.google.com)
    * Tools > Script editor
    * Clear the default empty function and paste the contents of [converttomarkdown.gapps](https://github.com/reallyfancy/gdocs2md/blob/master/converttomarkdown.gapps) into the code editor
    * Save
    
  * Running the script:
    - Tools > Script editor
    - Select "ConvertToMarkdown" function
    - Click Run button
    - If this is the first time you've run this script, authorise it when prompted
    - Converted doc with images attached will be emailed to you


## Interpreted formats
  * Text:
    * paragraphs are separated by two newlines
    * text styled as heading 1, 2, 3, etc is converted to Markdown heading: #, ##, ###, etc
    * text formatted with Courier New is backquoted: ``text``
    * links are converted to MD format: `[anchortext](url)`
  * Lists:
    * Numbered lists are converted correctly, including nested lists
    * bullet lists are converted to "`*`" Markdown format appropriately, including nested lists
  * Images:
    * images are correctly extracted and sent as attachments
  * Blocks:
    * Table of contents is replaced by `[[TOC]]`
    * blocks of text delimited by "--- class whateverclassnameyouwant" and "---" are converted to `<div class="whateverclassnameyouwant"></div>` 
    * Source code: 
      * blocks of text delimited by "--- source code" or "--- src" and "---" are converted to `<pre></pre>`
      * blocks of text delimited by "--- source pretty" or "--- srcp" and "---" are converted to `<pre class="prettyprint"></pre>`
    * Tables:
      * Simple `<table>` processing
