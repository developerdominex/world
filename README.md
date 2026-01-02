# Starlight JSON Utility

**Package:** starlight-json  
**Purpose:** Simple and safe JSON handling utilities for the Starlight programming language and server-side JavaScript environments.  
**Developer:** Dominex Macedon  

## Overview
This package provides helper functions to safely parse, stringify, validate, clone, and pretty-print JSON data.  
All functions are designed to fail gracefully and return `null` or `false` instead of throwing errors.

## Installation
`npm install starlight-json`

## Import
`
import json from "starlight-json";
`

## Functions

**parse(text)**  
Safely parses a JSON string.

`
let data = json.parse('{"name":"Starlight"}');
`

Returns parsed object or `null` if invalid.

---

**stringify(obj)**  
Converts an object into a JSON string.

`
let text = json.stringify({ language: "Starlight" });
`

Returns string or `null` if conversion fails.

---

**pretty(obj, space = 2)**  
Formats JSON with indentation for readability.

`
let formatted = json.pretty({ a: 1, b: 2 }, 4);
`

Returns formatted JSON string or `null`.

---

**clone(obj)**  
Creates a deep copy of an object using JSON serialization.

`
let copy = json.clone(originalObject);
`

Returns cloned object or `null`.

---

**isValid(text)**  
Checks whether a string is valid JSON.

`
let ok = json.isValid('{"valid":true}');
`

Returns `true` or `false`.

## Use Cases
• Handling API responses  
• Validating configuration files  
• Deep cloning simple objects  
• Safe JSON parsing in servers  
• Logging and debugging structured data  

## Notes
• Functions never throw errors  
• Best suited for JSON-safe data (no functions or circular references)  
• Ideal for backend and tooling utilities in Starlight  

## Author
**Developer:** Dominex Macedon
