# Grok Sidebar Assistant

A Chrome side panel extension that lets you ask Grok questions about the
current page. It extracts readable page text, YouTube transcripts, and PDF
content, then sends that context to Grok through OpenRouter.

## Features
- Side panel chat UI with history
- Page-aware answers using Readability
- YouTube transcript extraction
- PDF text extraction (up to 50 pages)
- File upload support for images and text/PDF files
- Markdown rendering for responses

## Requirements
- Chrome (Manifest V3 support)
- An OpenRouter API key

## Setup
1. Clone this repo.
2. Open `config.js` and set your key:
   - `OPENROUTER_API_KEY: "your-key"`
3. In Chrome, open `chrome://extensions/`.
4. Enable Developer mode.
5. Click "Load unpacked" and select this folder.

## Usage
1. Navigate to any webpage.
2. Click the extension icon to open the side panel.
3. Ask a question about the page, or upload a file for analysis.

## Notes
- The extension sends page content and recent chat history to OpenRouter.
- If you paste or upload sensitive content, it will be sent to the model.

## Troubleshooting
- If you see "Failed to fetch" errors, confirm:
  - You set a valid OpenRouter API key in `config.js`.
  - The extension has `https://openrouter.ai/*` in host permissions.

## Development
- Main UI: `sidebar.html`, `sidebar.css`, `sidebar.js`
- Background worker: `background.js`
- Content extraction: `content.js`

