# 📚 PDF Merger & Splitter

Merge multiple PDF files into one or split PDFs into individual pages! Features:
- **Merge:** Combine multiple PDFs with custom page ranges
- **Split:** Extract specific pages or split by page count
- **Reorder:** Custom page ordering and arrangement
- **Metadata:** Preserve or update document information
- **Watermark:** Add watermarks during merge process

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
   # Merge all PDFs in a folder
   operation = "merge"
   path_arg = "/path/to/pdfs/"
   
   # Split a PDF into individual pages
   operation = "split"
   path_arg = "document.pdf"
   
   # Add watermark during merge
   add_watermark = True
   watermark_text = "CONFIDENTIAL"
   ```

4. **Run all cells to process**

## 📁 Output
- Merge → `pdfs_merged.pdf`
- Split → Individual page files or custom ranges
