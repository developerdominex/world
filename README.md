# starlight-fs

**File System Utilities for Starlight Programming Language**

starlight-fs provides simple, safe, and synchronous file system operations designed specifically for server-side Starlight programs.  
It wraps Node.js fs and path modules into a clean API usable inside Starlight.

## Installation

`
npm install starlight-fs
`

## Import

`
import fs from "starlight-fs";
`

## Core File Operations

**Read a text file**  
`
let content = fs.readFile("data.txt");
`

Returns file content as string or null if file does not exist.

**Write a text file**  
`
fs.writeFile("data.txt", "Hello Starlight");
`

Returns true on success, false on failure.

**Append to a file**  
`
fs.appendFile("log.txt", "New line");
`

**Delete a file**  
`
fs.deleteFile("old.txt");
`

## JSON Utilities

**Read JSON file**  
`
let data = fs.readJSON("config.json");
`

Returns parsed object or null if invalid.

**Write JSON file**  
`
fs.writeJSON("config.json", { port: 3000 });
`

Automatically formats JSON with indentation.

## Directory Operations

**Create directory**  
`
fs.makeDir("storage");
`

**List directory contents**  
`
let files = fs.listDir("storage");
`

**Delete directory recursively**  
`
fs.deleteDir("storage");
`

## Copy Utilities

**Copy a file**  
`
fs.copyFile("a.txt", "b.txt");
`

**Copy a directory recursively**  
`
fs.copyDir("src", "backup");
`

## Path Utilities

**Join paths**  
`
let p = fs.join("a", "b", "file.txt");
`

**Get base name**  
`
fs.basename("/path/to/file.txt");
`

**Get directory name**  
`
fs.dirname("/path/to/file.txt");
`

**Get extension**  
`
fs.extname("file.txt");
`

**Resolve absolute path**  
`
fs.resolve("data", "file.txt");
`

## Server-Side Usage

starlight-fs is intended for:
- Server-side scripting
- CLI tools
- File-based storage
- Configuration handling
- Build tools
- PDF, JSON, and data pipelines

It is not designed for browser environments.

## Error Handling Philosophy

All operations fail safely.  
Instead of throwing errors, functions return:
- null
- false
- empty arrays

This keeps Starlight scripts predictable and stable.

## Author

**Developer:** Dominex Macedon

## Learning Hub

Starlight Language Documentation
