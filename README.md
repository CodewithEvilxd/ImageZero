# ImageZero

**Client-side image converter and compressor. Zero uploads. Complete privacy.**

ImageZero is a powerful web application that allows you to convert and compress images directly in your browser without uploading files to any server. Built with privacy and performance in mind, it processes all images locally using WebAssembly for lightning-fast operations.

## ✨ Key Features

### 🔒 Privacy First
- **Zero Uploads**: All processing happens locally in your browser
- **No Data Transmission**: Your images never leave your device
- **Complete Privacy**: No tracking, no analytics, no server-side processing

### 🚀 High Performance
- **WebAssembly Powered**: Rust-based image processing for maximum speed
- **Batch Processing**: Handle multiple images simultaneously
- **Real-time Preview**: Instant visual feedback during processing

### 🛠️ Comprehensive Tools
- **Format Conversion**: Convert between 9+ image formats
- **Quality Compression**: Lossy compression with adjustable quality
- **Drag & Drop Interface**: Intuitive file handling
- **ZIP Export**: Download multiple processed images as a single archive

### 🎨 Supported Formats
- **Input**: JPG, PNG, WebP, HEIC, GIF, BMP, ICO, TIFF, PNM
- **Output**: JPG, PNG, WebP (with compression support)
- **Special Handling**: Native HEIC support with fallback conversion

## 🏗️ Architecture

### Frontend
- **Framework**: Next.js 15 with App Router
- **Language**: TypeScript for type safety
- **Styling**: Tailwind CSS with custom gradients and animations
- **UI Components**: Radix UI primitives with custom styling
- **Animations**: Framer Motion for smooth interactions

### Backend (Client-side)
- **WebAssembly**: Rust compiled to WASM for high-performance image processing
- **Libraries**:
  - `image` crate for core image operations
  - Custom compression algorithms
  - Format conversion utilities

### Key Dependencies
- **heic2any**: HEIC file preprocessing
- **jszip**: Multi-file ZIP generation
- **sonner**: Toast notifications
- **lucide-react**: Modern icon library

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- Rust 1.70+ (for WebAssembly compilation)
- pnpm/npm/yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/codewithevilxd/imagezero.git
   cd imagezero
   ```

2. **Install dependencies**
   ```bash
   pnpm install
   ```

3. **Build WebAssembly module**
   ```bash
   cd wasm
   wasm-pack build --target web --out-dir pkg
   cd ..
   ```

4. **Start development server**
   ```bash
   pnpm dev
   ```

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📖 Usage

### Image Conversion
1. Select the "Converter" tab
2. Upload images via drag & drop or file picker
3. Choose target format from the dropdown
4. Click "Convert" to process images
5. Download individual files or ZIP archive

### Image Compression
1. Select the "Compressor" tab
2. Upload images to compress
3. Adjust quality slider (1-100%)
4. Click "Compress" to process
5. Download compressed results

### Batch Processing
- Upload multiple images at once
- All files are processed in parallel
- Progress tracking for each image
- Bulk download as ZIP file

## 🔧 Development

### Project Structure
```
imagezero/
├── app/                    # Next.js app directory
│   ├── layout.tsx         # Root layout
│   ├── page.tsx           # Main page
│   └── globals.css        # Global styles
├── components/            # React components
│   ├── navbar.tsx         # Navigation component
│   ├── compressor/        # Compression interface
│   └── convertor/         # Conversion interface
├── lib/                   # Utility functions
├── wasm/                  # WebAssembly module
│   ├── src/              # Rust source code
│   └── Cargo.toml        # Rust dependencies
└── public/               # Static assets
```

### Building for Production
```bash
# Build the application
pnpm build

# Start production server
pnpm start
```

### WebAssembly Development
The WebAssembly module is written in Rust and provides the core image processing functionality.

```bash
cd wasm

# Development build
wasm-pack build --target web --out-dir pkg --dev

# Optimized production build
wasm-pack build --target web --out-dir pkg --release
```

## 🎯 Core Algorithms

### Image Conversion
- Format detection and validation
- Color space conversion
- Metadata preservation
- Quality optimization

### Compression
- Lossy compression with quality control
- File size optimization
- Visual quality preservation
- Format-specific optimizations

### WebAssembly Integration
- Memory-efficient processing
- Parallel image handling
- Error handling and recovery
- Type-safe Rust-TypeScript interface

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow TypeScript strict mode
- Write comprehensive tests
- Update documentation
- Maintain code quality standards

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) - The React framework
- [Rust](https://www.rust-lang.org/) - Systems programming language
- [WebAssembly](https://webassembly.org/) - Binary instruction format
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
- [Radix UI](https://www.radix-ui.com/) - Low-level UI primitives

## 📞 Support

If you have any questions or need help:

- Open an issue on GitHub
- Check the documentation
- Review existing issues for similar problems

---

**Built with ❤️ using Rust, WebAssembly, and Next.js**
