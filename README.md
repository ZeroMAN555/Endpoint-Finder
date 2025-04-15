# Endpoint-Finder
![EndpointFinder Banner](https://raw.githubusercontent.com/ZeroMAN555/Endpoint-Finder/refs/heads/main/banner.png)
A powerful browser-based tool for discovering URLs and endpoints on web pages.

## 🌟 Overview

EndpointFinder is a JavaScript bookmarklet that helps security researchers, web developers, and QA testers discover and categorize all endpoints and URLs on a web page. It scans the DOM, JavaScript, and network requests to find hidden endpoints that might not be immediately visible.

## ✨ Features

- **Real-time scanning** of the current web page
- **Categorizes endpoints** into four types:
  - 🔌 API Endpoints
  - 🔗 Internal URLs
  - 🖼️ Asset URLs 
  - 🌐 External URLs
- **Filter results** dynamically by text search or endpoint type
- **Copy to clipboard** functionality for individual endpoints or all results
- **Clean, intuitive UI** with a modern dark theme (Dracula-inspired)
- **Zero dependencies** - runs directly in your browser console

## 📋 Installation

### Option 1: Browser Console

1. Open your browser's developer console (F12 or Right-click > Inspect > Console)
2. Copy the entire code from `endpoint-finder.js`
3. Paste it into the console and press Enter

### Option 2: Create a Bookmarklet

1. Create a new bookmark in your browser
2. Name it "EndpointFinder"
3. In the URL/Location field, paste the following:
```
javascript:(function(){PASTE_CODE_HERE})();
```
4. Save the bookmark
5. Click the bookmark on any web page to run EndpointFinder

## 🚀 Usage

1. After running the script, a panel will appear at the bottom of the web page
2. EndpointFinder will automatically scan the page and display all discovered endpoints
3. Use the filter input to search for specific endpoints
4. Use the dropdown to filter by endpoint type
5. Click on any endpoint to copy it to clipboard
6. Click "Copy All" to copy all visible endpoints
7. Click the X button to close EndpointFinder

## 💡 How It Works

EndpointFinder uses multiple techniques to discover endpoints:

1. Extracts URLs from DOM elements (`<a>`, `<script>`, `<img>`, `<link>`, `<form>`, `<iframe>`)
2. Parses the page's HTML to find URLs in attributes (`href`, `src`, `action`, etc.)
3. Searches JavaScript code for potential API endpoints
4. Analyzes the browser's Performance API for network requests

## 🔍 Endpoint Classification

- **API Endpoints**: URLs containing `/api/`, `/graphql/`, `/v1/`, `/v2/`, or matching specific patterns
- **Asset URLs**: Files with extensions like .jpg, .png, .css, .js, etc.
- **External URLs**: URLs pointing to domains different from the current one
- **Internal URLs**: All other URLs on the same domain

## 🛡️ Security Note

This tool is designed for ethical use in:
- Security research with proper authorization
- Development and testing of your own websites
- Educational purposes

Always obtain proper permission before scanning websites you don't own.
