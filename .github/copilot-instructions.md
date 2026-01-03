# WhatsApp Direct Link Generator - AI Agent Instructions

## Project Overview
This is a simple, single-file web application that generates direct WhatsApp chat links using the `wa.me` URL scheme. The entire application resides in `index.html` with inline CSS and JavaScript.

## Architecture
- **Single-page application**: All code (HTML, CSS, JS) in one file
- **No dependencies**: Pure vanilla JavaScript, no frameworks or libraries
- **Client-side only**: Runs entirely in the browser, no server required

## Key Components
- **Input fields**: Phone number (required) and message (optional)
- **Link generation**: Creates `https://wa.me/{phone}?text={encoded_message}` format
- **Basic validation**: Ensures phone number is provided
- **Direct link**: Opens WhatsApp web or app when clicked

## Development Workflow
- **No build process**: Edit `index.html` directly and open in browser
- **Testing**: Open in browser, enter test data, verify generated links work
- **Debugging**: Use browser dev tools console for JavaScript errors

## Code Patterns
- **URL encoding**: Always use `encodeURIComponent()` for message text to handle special characters
- **Phone format**: Expect numbers without + or spaces (e.g., "1234567890" not "+1 234 567 890")
- **Error handling**: Simple `alert()` for user feedback on invalid input
- **Styling**: Inline CSS for simplicity, basic responsive design

## File Structure
```
index.html          # Complete application
.github/
  copilot-instructions.md  # This file
```

## Common Tasks
- **Adding features**: Modify the `generateLink()` function in `<script>` tag
- **Styling changes**: Edit CSS in `<style>` tag
- **Input validation**: Enhance checks in `generateLink()` before link creation

## Integration Points
- **WhatsApp API**: Uses public `wa.me` URL scheme (no authentication required)
- **Browser compatibility**: Works in all modern browsers with URL opening support

## Deployment
- **Static hosting**: Upload `index.html` to any web server
- **Local testing**: Double-click file or use `python -m http.server` for local preview