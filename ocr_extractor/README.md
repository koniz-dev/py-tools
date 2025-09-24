# 🔍 OCR Text Extractor

Extract text from images using Optical Character Recognition! Features:
- Support for multiple languages (English, Vietnamese, Chinese, Japanese, Korean)
- Advanced image preprocessing for better accuracy
- Confidence scoring and word positioning
- Batch processing with detailed analysis

**Supported formats:** PNG, JPG, JPEG, WEBP, TIFF, BMP

## 🚀 Quick Start

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Install Tesseract OCR:**
   ```bash
   # Ubuntu/Debian
   sudo apt install tesseract-ocr tesseract-ocr-vie
   
   # macOS
   brew install tesseract
   
   # Windows: Download from GitHub
   ```

3. **Open the tool:**
   ```bash
   jupyter notebook tool.ipynb
   ```

4. **Configure your settings:**
   ```python
   # Single image
   path_arg = "screenshot.png"
   
   # Folder with images
   path_arg = "/path/to/images/"
   
   # Language settings
   language = "eng+vie"  # English and Vietnamese
   include_details = True
   ```

5. **Run all cells to extract text**

## 📁 Output
- `filename_ocr.txt` with extracted text and confidence scores
