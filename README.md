# Starlight TXT to PDF

**Purpose**
Starlight TXT to PDF converts a plain text file written in a simple DSL into a styled PDF.
It supports headers, colors, bold, italic, absolute positioning, images, and automatic pagination.

## Installation

` npm install starlight-txt-to-pdf `

## Basic Usage

` import { txtToPdf } from "starlight-txt-to-pdf";

await txtToPdf("input.txt", "output.pdf", {
header: "My Document Header"
});
`

## TXT DSL Syntax

**1. Headings**
Use hash-style headings inside the TXT file.

` # Title ## Section ### Sub Section `

**2. Bold Text**

` [b]This text is bold[/b] `

**3. Italic Text**

` [i]This text is italic[/i] `

**4. Colored Text**

` [color:red]Red Text[/color] [color:gray]Gray Text[/color] [color:blue]Blue Text[/color] `

Supported colors:
red, green, blue, yellow, cyan, magenta, gray, white, black

**5. Absolute Positioned Text**
Draw text at an exact X,Y position on the page.

` [pos:430,120][color:gray]— Macedon[/color][/pos] `

Coordinates are in PDF points.

**6. Images**
Embed images anywhere on the page.

` [img:logo.png,x=450,y=50,w=80,h=80] `

Supported formats: PNG, JPG, JPEG

## Page Layout

• Automatic page breaks
• Header shown on every page
• Footer with page number
• Margins handled internally

Header text can be customized using options.

## Options

**header**
Text shown at the top of every page.

` { header: "My Custom Header" } `

## Example TXT File

` # Love Letter

[color:red]My Dearest[/color]

This document was generated using Starlight.

[pos:420,100][color:gray]— Dominex Macedon[/color][/pos]

[img:logo.png,x=460,y=40,w=60,h=60]
`

## Output

• Clean PDF layout
• Styled text
• Images embedded
• Multi-page support

## Notes

• TXT file must exist
• Image paths must be valid
• Colors are predefined
• Absolute positioning overrides flow layout

## Developer

**Developer - Dominex Macedon**

https://starlight-learn-lang.pages.dev/
