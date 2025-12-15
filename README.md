# Image Buddy

A simple, privacy-focused image converter and compressor that runs entirely in your browser. No uploads, no servers, no tracking—just pure client-side image processing.

## Features

- **100% Client-Side Processing** - All image conversion happens in your browser. Your images never leave your device.
- **Multiple Format Support** - Convert images to WebP, JPEG, or PNG
- **Quality Control** - Adjustable compression settings (40-95%)
- **Batch Processing** - Handle multiple images at once
- **Drag & Drop** - Intuitive file handling with drag-and-drop support
- **Paste Support** - Paste images directly from clipboard (Cmd/Ctrl+V)
- **File Renaming** - Customize output filenames before downloading
- **Size Comparison** - See original vs. converted file sizes
- **Mobile Friendly** - Responsive design that works on all devices

## How to Use

1. **Add Images**: Drop files, paste from clipboard, or click "Choose files"
2. **Select Format**: Choose WebP, JPEG, or PNG as output format
3. **Adjust Quality**: Set compression level (higher = better quality, larger file)
4. **Process**: Click "Process all" to convert all images
5. **Download**: Download individual images or process and download in batch

## Live Demo

Visit the live app: [https://skrulling.github.io/image-buddy](https://skrulling.github.io/image-buddy)

## Local Development

Simply open `index.html` in a modern web browser. No build step or dependencies required.

```bash
# Clone the repository
git clone https://github.com/skrulling/image-buddy.git

# Open in browser
open index.html
```

## Deployment to GitHub Pages

1. **Push to GitHub**:
   ```bash
   git remote add origin https://github.com/skrulling/image-buddy.git
   git branch -M main
   git push -u origin main
   ```

2. **Enable GitHub Pages**:
   - Go to your repository settings
   - Navigate to "Pages" in the sidebar
   - Under "Source", select "Deploy from a branch"
   - Select the `main` branch and `/ (root)` folder
   - Click "Save"

3. **Access Your Site**:
   - Your site will be available at `https://skrulling.github.io/image-buddy`
   - It may take a few minutes for the initial deployment

## How It Works

Image Buddy uses the HTML5 Canvas API to process images entirely in the browser:

1. Images are read as Data URLs using the FileReader API
2. Canvas API loads and renders the image
3. `toBlob()` converts the canvas to the desired format with specified quality
4. Processed images are made available for download via Object URLs

**Privacy**: Since everything happens in your browser, your images are never uploaded to any server. The app works completely offline after the initial page load.

## Technologies

- **Vanilla JavaScript** - No frameworks, no dependencies
- **HTML5 Canvas API** - For image processing
- **CSS3** - Modern styling with custom properties
- **Web APIs** - FileReader, Blob, Clipboard, Drag & Drop

## Browser Support

Works in all modern browsers that support:
- HTML5 Canvas API
- FileReader API
- Blob API
- ES6+ JavaScript

Tested on:
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+

## License

MIT License - Feel free to use, modify, and distribute as needed.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

---

Made with care for privacy-conscious users who want simple, fast image conversion without cloud uploads.
