# 📸 Image to PDF Converter

Convert images to PDF files easily! Supports:
- Single images
- Multiple images (creates ZIP file)
- ZIP files containing images
- Folders with images

**Supported formats:** PNG, JPG, JPEG, WEBP

## 🚀 Quick Start

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Open the tool:**
   ```bash
   jupyter notebook tool.ipynb
   ```

3. **Configure your settings:**
   ```python
   # Single image
   path_arg = "photo.jpg"
   
   # Folder with images  
   path_arg = "/path/to/images/"
   
   # ZIP file
   path_arg = "images.zip"
   ```

4. **Run all cells to convert**

## 📁 Output
- Single image → `filename.pdf`
- Multiple images → `images_pdfs.zip` (contains multiple PDFs)
