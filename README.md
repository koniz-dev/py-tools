# 🐍 Py-Tools

A comprehensive collection of Python utilities for document processing, image manipulation, and web scraping. This project provides easy-to-use Jupyter notebooks with advanced features for various file format conversions and analysis.

## 📋 Features

### 🖼️ Image to PDF Converter (`image2pdf.ipynb`)
- Convert single images to PDF
- Batch convert multiple images to individual PDFs
- Process ZIP files containing images
- Scan folders for images and convert them
- **Supported formats:** PNG, JPG, JPEG, WEBP
- Automatic ZIP creation for multiple files
- Google Colab compatible


### 🔍 OCR Text Extractor (`ocr_extractor.ipynb`)
- Extract text from images using Optical Character Recognition
- Support for multiple languages (English, Vietnamese, Chinese, Japanese, Korean)
- Advanced image preprocessing for better accuracy
- Confidence scoring and word positioning
- Batch processing with detailed analysis
- **Supported formats:** PNG, JPG, JPEG, WEBP, TIFF, BMP
- Language auto-detection and manual selection
- Google Colab compatible

### 📚 PDF Merger & Splitter (`pdf_merger.ipynb`)
- Merge multiple PDF files into one document
- Split PDFs into individual pages or custom page ranges
- Custom page ordering and arrangement
- Watermark addition during merge process
- Metadata preservation and analysis
- Batch processing with detailed statistics
- Advanced PDF manipulation features
- Google Colab compatible

### 📊 Document Analyzer (`document_analyzer.ipynb`)
- Comprehensive document metadata extraction
- Content analysis with readability scores
- Security analysis (encryption, permissions)
- File hash calculation (MD5, SHA256)
- Batch processing with detailed reports
- **Supported formats:** PDF, DOCX, TXT, RTF, HTML, MD
- Word frequency analysis and statistics
- JSON and text report generation
- Google Colab compatible

### 🌐 Web Scraper & PDF Converter (`web_scraper.ipynb`)
- Convert web pages to PDF documents
- Full-page screenshot capture
- Website crawling with automatic link discovery
- Custom CSS styling for better PDF output
- Mobile view simulation
- Headless browsing with JavaScript support
- Batch URL processing
- Advanced web scraping capabilities
- Google Colab compatible

## 🚀 Quick Start

### Prerequisites
- Python 3.8+ (recommended: Python 3.9+)
- Jupyter Notebook or Google Colab
- For OCR: Tesseract OCR engine (see installation notes below)

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd py-tools
   ```

2. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

### Additional Setup for OCR

For OCR functionality, you need to install Tesseract OCR:

**Windows:**
```bash
# Download and install from: https://github.com/UB-Mannheim/tesseract/wiki
# Add to PATH: C:\Program Files\Tesseract-OCR
```

**macOS:**
```bash
brew install tesseract
```

**Linux (Ubuntu/Debian):**
```bash
sudo apt update
sudo apt install tesseract-ocr
sudo apt install tesseract-ocr-vie  # For Vietnamese support
```

**Google Colab:**
```bash
# Tesseract is pre-installed, just install language packs if needed
!apt install tesseract-ocr-vie
```

### Usage

#### Image to PDF Conversion
1. Open `image2pdf.ipynb`
2. Set your file path in the configuration cell:
   ```python
   path_arg = "path/to/your/image.jpg"  # Single image
   path_arg = "path/to/images/"         # Folder
   path_arg = "images.zip"              # ZIP file
   ```
3. Run all cells to convert


#### OCR Text Extraction
1. Open `ocr_extractor.ipynb`
2. Configure your settings:
   ```python
   path_arg = "screenshot.png"          # Single image
   path_arg = "path/to/images/"         # Folder
   language = "auto"                    # Auto-detect or specify
   include_details = True               # Detailed analysis
   ```
3. Run all cells to extract text

#### PDF Merging & Splitting
1. Open `pdf_merger.ipynb`
2. Configure your settings:
   ```python
   operation = "merge"                  # "merge", "split", "merge_custom"
   path_arg = "path/to/pdfs/"           # Folder with PDFs
   add_watermark = False                # Add watermark
   split_mode = "pages"                 # Split mode
   ```
3. Run all cells to process

#### Document Analysis
1. Open `document_analyzer.ipynb`
2. Configure your settings:
   ```python
   path_arg = "document.pdf"            # Single document
   path_arg = "path/to/documents/"      # Folder
   include_hashes = True                # Calculate file hashes
   detailed_analysis = True             # Full analysis
   ```
3. Run all cells to analyze

#### Web Scraping & PDF Conversion
1. Open `web_scraper.ipynb`
2. Configure your settings:
   ```python
   urls = ["https://example.com"]       # URLs to convert
   mode = "pdf"                         # "pdf" or "screenshot"
   crawl_mode = False                   # Enable crawling
   headless = True                      # Headless browser
   ```
3. Run all cells to convert

## 📁 Project Structure

```
py-tools/
├── image2pdf.ipynb          # Image to PDF converter
├── ocr_extractor.ipynb      # OCR text extractor
├── pdf_merger.ipynb         # PDF merger & splitter
├── document_analyzer.ipynb  # Document analyzer
├── web_scraper.ipynb        # Web scraper & PDF converter
├── requirements.txt         # Python dependencies
└── README.md                # This file
```

## 🔧 Features in Detail

### Image to PDF Converter
- **Smart file detection:** Automatically handles files, folders, and ZIP archives
- **Batch processing:** Converts multiple images efficiently
- **Format support:** PNG, JPG, JPEG, WEBP
- **Output options:** Single PDF or ZIP with multiple PDFs
- **Colab integration:** Direct download in Google Colab environment


### OCR Text Extractor
- **Multi-language support:** English, Vietnamese, Chinese, Japanese, Korean
- **Advanced preprocessing:** Image enhancement for better accuracy
- **Confidence scoring:** Quality assessment for extracted text
- **Word positioning:** Detailed bounding box information
- **Batch processing:** Handle multiple images efficiently
- **Language detection:** Automatic language identification

### PDF Merger & Splitter
- **Flexible merging:** Combine multiple PDFs with custom page ranges
- **Smart splitting:** Extract pages by count or individual pages
- **Watermark support:** Add custom watermarks during merge
- **Metadata preservation:** Maintain document information
- **Custom ordering:** Arrange pages in any sequence
- **Batch operations:** Process multiple files simultaneously

### Document Analyzer
- **Comprehensive analysis:** Metadata, content, and security analysis
- **Readability scoring:** Flesch-Kincaid and other readability metrics
- **Security assessment:** Encryption and permission analysis
- **File integrity:** MD5 and SHA256 hash calculation
- **Content statistics:** Word count, frequency analysis
- **Multi-format support:** PDF, DOCX, TXT, RTF, HTML, MD

### Web Scraper & PDF Converter
- **Headless browsing:** Full JavaScript support with Selenium
- **Website crawling:** Automatic link discovery and following
- **Custom styling:** CSS modifications for better PDF output
- **Mobile simulation:** Test mobile-responsive designs
- **Screenshot mode:** Full-page image capture
- **Batch processing:** Convert multiple URLs efficiently

## 🌐 Google Colab Support

All notebooks are fully compatible with Google Colab:
- Automatic package installation
- File upload interface
- Direct download of results
- No local setup required
- Headless browser support
- OCR language packs

## 📝 Examples

### Convert a single image
```python
path_arg = "photo.jpg"
# Output: photo.pdf
```

### Convert a folder of images
```python
path_arg = "/path/to/images/"
# Output: images_pdfs.zip (contains multiple PDFs)
```


### Extract text from image
```python
path_arg = "screenshot.png"
language = "eng+vie"  # English and Vietnamese
# Output: screenshot_ocr.txt (with confidence scores)
```

### Merge PDFs with watermark
```python
operation = "merge"
path_arg = "path/to/pdfs/"
add_watermark = True
watermark_text = "CONFIDENTIAL"
# Output: pdfs_merged.pdf
```

### Analyze document metadata
```python
path_arg = "document.pdf"
include_hashes = True
# Output: document_analysis.txt (detailed report)
```

### Convert website to PDF
```python
urls = ["https://example.com"]
mode = "pdf"
custom_css = "nav { display: none; }"
# Output: example_com_index.pdf
```

## 🛠️ Dependencies

### Core Libraries
- **Pillow (PIL):** Image processing
- **pdfplumber:** PDF text extraction
- **PyMuPDF (fitz):** PDF manipulation
- **PyPDF2:** PDF merging and splitting
- **reportlab:** PDF generation and watermarks

### OCR & Analysis
- **pytesseract:** Optical Character Recognition
- **opencv-python:** Image preprocessing
- **python-docx:** Word document processing
- **python-magic:** File type detection
- **textstat:** Readability analysis

### Web Scraping
- **selenium:** Web browser automation
- **webdriver-manager:** Chrome driver management
- **beautifulsoup4:** HTML parsing
- **requests:** HTTP requests

### Standard Libraries
- **os, zipfile, shutil, uuid, pathlib:** File operations
- **json, re, time, datetime:** Data processing
- **hashlib, collections:** Utilities

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 🔧 Troubleshooting

### Common Issues

**OCR not working:**
- Ensure Tesseract is installed and in your PATH
- Check language packs are installed for your target languages
- Try different image preprocessing settings

**PDF processing errors:**
- Ensure PDF files are not password-protected
- Check file permissions and disk space
- Try with smaller files first

**Web scraping issues:**
- Update Chrome/Chromium browser
- Check internet connection
- Some sites may block automated access

**Memory issues with large files:**
- Process files in smaller batches
- Use Google Colab for better memory management
- Consider file compression before processing

### Performance Tips

- Use Google Colab for better performance and memory
- Process files in batches for large datasets
- Enable headless mode for web scraping
- Use appropriate image quality settings for OCR

## 📞 Support

If you encounter any issues or have questions, please open an issue on the repository.

## 🆕 Recent Updates

- ✅ Added comprehensive requirements.txt
- ✅ Improved installation instructions
- ✅ Enhanced OCR setup guide
- ✅ Added troubleshooting section
- ✅ Updated project structure documentation

---

**Made with ❤️ for easy document processing**
