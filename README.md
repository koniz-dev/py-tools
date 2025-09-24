# 🐍 Py-Tools

A collection of useful Python utilities for document and image processing. This project provides easy-to-use Jupyter notebooks for converting between different file formats.

## 📋 Features

### 🖼️ Image to PDF Converter (`image2pdf.ipynb`)
- Convert single images to PDF
- Batch convert multiple images to individual PDFs
- Process ZIP files containing images
- Scan folders for images and convert them
- **Supported formats:** PNG, JPG, JPEG, WEBP
- Automatic ZIP creation for multiple files
- Google Colab compatible

### 📄 PDF to HTML Converter (`pdf2html.ipynb`)
- Convert PDF files to clean HTML format
- Preserve text content and basic formatting
- Extract and display table structures
- Optional image extraction with positioning info
- Process single PDFs, folders, or ZIP files
- Responsive HTML output with modern styling
- Google Colab compatible

## 🚀 Quick Start

### Prerequisites
- Python 3.6+
- Jupyter Notebook or Google Colab

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd py-tools
   ```

2. **Install required packages:**
   ```bash
   pip install pillow pdfplumber PyMuPDF
   ```

3. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
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

#### PDF to HTML Conversion
1. Open `pdf2html.ipynb`
2. Configure your settings:
   ```python
   path_arg = "document.pdf"            # Single PDF
   path_arg = "path/to/pdfs/"           # Folder
   path_arg = "documents.zip"           # ZIP file
   extract_images = True                # Include image info
   ```
3. Run all cells to convert

## 📁 Project Structure

```
py-tools/
├── image2pdf.ipynb          # Image to PDF converter
├── pdf2html.ipynb           # PDF to HTML converter
└── README.md                # This file
```

## 🔧 Features in Detail

### Image to PDF Converter
- **Smart file detection:** Automatically handles files, folders, and ZIP archives
- **Batch processing:** Converts multiple images efficiently
- **Format support:** PNG, JPG, JPEG, WEBP
- **Output options:** Single PDF or ZIP with multiple PDFs
- **Colab integration:** Direct download in Google Colab environment

### PDF to HTML Converter
- **Advanced text extraction:** Preserves formatting and layout
- **Table recognition:** Converts PDF tables to HTML tables
- **Image handling:** Extracts image information and positioning
- **Responsive design:** Clean, modern HTML output
- **Font analysis:** Detects bold, italic, and size variations
- **Page structure:** Maintains page breaks and numbering

## 🌐 Google Colab Support

Both notebooks are fully compatible with Google Colab:
- Automatic package installation
- File upload interface
- Direct download of results
- No local setup required

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

### Convert PDF with images
```python
path_arg = "document.pdf"
extract_images = True
# Output: document.html (with image placeholders)
```

## 🛠️ Dependencies

- **Pillow (PIL):** Image processing
- **pdfplumber:** PDF text extraction
- **PyMuPDF (fitz):** PDF manipulation
- **Standard libraries:** os, zipfile, shutil, uuid, pathlib

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

If you encounter any issues or have questions, please open an issue on the repository.

---

**Made with ❤️ for easy document processing**
