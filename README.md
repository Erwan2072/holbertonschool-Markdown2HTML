# Markdown2HTML

Markdown2HTML is a Python script that converts Markdown files into HTML. This script handles headings, unordered and ordered lists, simple paragraphs, bold text, emphasis, and custom syntax transformations.

## Requirements

- Ubuntu 18.04 LTS
- Python 3.7 or higher
- PEP 8 style guide compliance (version 1.7.*)
- All scripts are executable and documented.
- Custom Markdown features, including transformations like `[[text]]` (MD5 conversion) and `((text))` (character removal).

## Features

### Supported Markdown Syntax

| Markdown Syntax          | HTML Output                               | Description                                           |
|---------------------------|-------------------------------------------|-------------------------------------------------------|
| `# Heading level 1`       | `<h1>Heading level 1</h1>`               | Converts headings from level 1 to 6                  |
| `- List item`             | `<ul><li>List item</li></ul>`            | Converts unordered lists                             |
| `* List item`             | `<ol><li>List item</li></ol>`            | Converts ordered lists                               |
| `Hello`                   | `<p>Hello</p>`                           | Converts simple paragraphs                           |
| `**Bold text**`           | `<b>Bold text</b>`                       | Formats text in bold                                 |
| `__Italic text__`         | `<em>Italic text</em>`                   | Formats text in italics                              |
| `[[Text]]`                | `MD5 hash of "Text"`                     | Converts content to its MD5 hash                    |
| `((Text))`                | `Te` (removes all 'c' or 'C')            | Removes all 'c' (case insensitive) from content      |

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/holbertonschool-Markdown2HTML.git
   ```

2. Navigate to the project directory:
```
cd holbertonschool-Markdown2HTML
```
3.Ensure the script is executable:
```
chmod +x markdown2html.py
```
## Usage
Run the script using the following command:

```
./markdown2html.py input_file.md output_file.html
```

## Examples
Case 1: Missing arguments
```
$ ./markdown2html.py
Usage: ./markdown2html.py README.md README.html
```
Case 2: File conversion
Input (README.md):

```
# Title
- Item 1
- Item 2
**Bold**
__Italic__
[[Secret]]
((Chicago))
```
Output (README.html):

```
<h1>Title</h1>
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
</ul>
<p><b>Bold</b></p>
<p><em>Italic</em></p>
<p>2bb80d537b1da3e38bd30361aa855686</p>
<p>hiago</p>
```

## Development
Code Style
The code follows PEP 8 guidelines. Use the following to check compliance:

```
pycodestyle markdown2html.py
```
