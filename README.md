# OPML to Text Converter

This Python script converts OPML (Outline Processor Markup Language) files to a simple text format. It preserves the hierarchical structure of the OPML and includes both the text and description attributes in the output.

## Features

- Converts OPML to a simple, readable text format
- Preserves hierarchy using dot notation
- Handles nested outlines of any depth
- Reads from stdin and writes to stdout for easy integration with other tools
- No external dependencies - uses only Python standard library

## Requirements

- Python 3.6 or higher

## Installation

Clone this repository:

```
$ git clone https://github.com/rinodrops/opml2txt.git
$ cd opml2txt
```

No additional installation steps are required as the script uses only Python standard libraries.

## Usage

Run the script and pipe the OPML content to it

```
$ cat input.opml | python ompl2txt > output.txt
```

Or use input redirection

```
python opml2txt < input.opml > output.txt
```

### Input Format

The input should be a valid OPML file. Example:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<opml version="2.0">
  <head>
    <title>Sample OPML</title>
  </head>
  <body>
    <outline text="Category1" Description="Description1">
      <outline text="Subcategory1" Description="Subdescription1"/>
    </outline>
  </body>
</opml>
```

### Output Format

The output will be in the following format:

```
.Category1: Description1
.Category1.Subcategory1: Subdescription1
```

### License

This project is licensed under the MIT License - see the LICENSE file for details.
