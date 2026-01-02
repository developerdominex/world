# Starlight Color Utilities

**Package:** starlight-color  
**Author:** Dominex Macedon  

## Description
Use this package to style terminal output with colors in Starlight Programming Language. Supports standard colors, bright colors, and gray scale.

## Installation
`npm install starlight-color`

## Usage
**Importing the package:**
`
import * as color from "starlight-color";
`

**Examples:**
`
sldeploy color.red("This text is red");
sldeploy color.green("This text is green");
sldeploy color.brightBlue("Bright blue text");
sldeploy color.gray("Gray text");
`

## Available Colors
- red, green, yellow, blue, magenta, cyan, white, gray  
- brightRed, brightGreen, brightYellow, brightBlue, brightMagenta, brightCyan, brightWhite  

## Notes
This library only affects terminal output. It works in Node.js CLI environments and supports ANSI color codes.

**Developer:** Dominex Macedon
