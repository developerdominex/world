starlight-pdf

starlight-pdf is a server-side utility package for the Starlight Programming Language ecosystem that provides PDF processing features for Node.js environments.
It allows developers to convert PDF files into images and rebuild PDFs from image files, making it suitable for previews, transformations, and document pipelines.

This package is intended for developer and backend use only and is not designed for browser environments.

Features

Convert each page of a PDF into high-quality PNG images

Rebuild a PDF from a list of image files

Uses stable libraries such as pdfjs-dist, canvas, and pdf-lib

Fully compatible with ES Modules

Safe worker and path handling for Node.js

Installation

Install using npm:

npm install starlight-pdf

Requirements

This package runs in a Node.js environment and requires native dependencies.

Node.js

Node.js version 16 or later is recommended.

Native Dependencies

Because this package uses canvas, system-level libraries are required.

Windows

Install windows-build-tools or use prebuilt canvas binaries when available.

Linux (Ubuntu / Debian)

sudo apt install libcairo2-dev libpango1.0-dev libjpeg-dev libgif-dev librsvg2-dev

macOS

brew install pkg-config cairo pango libpng jpeg giflib librsvg

Usage
Importing the Module

import pdfUtils from "starlight-pdf";

Convert PDF to Images

await pdfUtils.pdfToImages(
"./input.pdf",
"./output-images"
);

Result:

Each page is rendered as page-1.png, page-2.png, and so on

Images are rendered at high resolution

Convert Images Back to PDF

await pdfUtils.imagesToPdf(
[
"./output-images/page-1.png",
"./output-images/page-2.png"
],
"./output.pdf"
);

Result:

A new PDF is created using the provided images

Image dimensions are preserved exactly

API Reference
pdfToImages(pdfPath, outputDir)

Converts a PDF into PNG images.

Parameters:

pdfPath (string): Path to the source PDF

outputDir (string): Directory where images will be saved

Returns:

Promise<string[]> — Array of generated image file paths

imagesToPdf(imagePaths, outputPdf)

Creates a PDF from image files.

Parameters:

imagePaths (string[]): Array of image paths (PNG or JPG)

outputPdf (string): Output PDF file path

Returns:

Promise<string> — Output PDF path

Internal Notes

Uses pdfjs-dist legacy build for Node.js compatibility

Worker source is resolved manually to prevent runtime errors

Uses canvas for rendering and pdf-lib for PDF generation

Fully compatible with ES Module syntax

Starlight Ecosystem

This package is part of the Starlight Programming Language ecosystem and is designed to work alongside other Starlight packages such as:

starlight-cli

starlight-fs

starlight-api

starlight-time

starlight-color

Learning hub and documentation:
https://starlight-learn-lang.pages.dev/

License

MIT License

Author

developerdominex

Built for developers who need reliable server-side document processing within the Starlight ecosystem.
