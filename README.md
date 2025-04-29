# R3D to AVI Converter

A browser-based converter for RED Digital Cinema R3D files to AVI format using WebAssembly technology.

## Features

- **Browser-based conversion**: No server uploads required
- **Memory-optimized processing**: Handles large R3D files up to 2GB
- **Chunked file processing**: Breaks large files into manageable pieces
- **Real-time memory monitoring**: Prevents browser crashes
- **Multi-threaded support**: Optional faster processing
- **Configurable encoding options**: Control quality and file size
- **Simple drag-and-drop interface**: Easy to use

## Technical Details

This application uses:
- FFmpeg.wasm for video processing in the browser
- React for the user interface
- Chunked file processing to handle large files
- Memory optimization techniques for browser constraints
- WebAssembly for near-native performance

## Installation

1. Clone this repository
2. Install dependencies:
```
npm install
```
3. Start the development server:
```
npm run dev
```

## Usage

1. Open the application in your browser
2. Toggle multi-threaded processing if desired (faster but uses more memory)
3. Drag and drop your R3D file onto the upload area
4. Click "Decode R3D" to extract the video data
5. Configure encoding options as needed
6. Click "Encode to AVI" to convert the file
7. Download the resulting AVI file

## Limitations

- Maximum file size: 2GB (WebAssembly limitation)
- Browser must support WebAssembly and SharedArrayBuffer
- For Chrome/Edge, the site must be served over HTTPS or localhost
- For Firefox, additional configuration may be required
- Processing large files requires significant system memory

## Browser Compatibility

- Chrome/Edge: Version 90+
- Firefox: Version 90+ (with SharedArrayBuffer enabled)
- Safari: Version 15+

## Development

### Building for production

```
npm run build
```

### Customizing

The application is built with modular components that can be extended:
- `ChunkedFileUpload`: Handles file selection and chunking
- `R3DDecoder`: Extracts video data from R3D files
- `AVIEncoder`: Converts video data to AVI format
- `FileDownload`: Manages the download process
- `MemoryMonitor`: Tracks and optimizes memory usage

## License

Limited Internal Evaluation License (IEI-RED-0426-CB)

## Acknowledgements

- FFmpeg.wasm project
- RED Digital Cinema for R3D format specifications
