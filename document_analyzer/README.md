# 📊 Document Analyzer

Comprehensive document analysis tool! Features:
- Document metadata extraction
- Content analysis with readability scores
- Security analysis (encryption, permissions)
- File hash calculation (MD5, SHA256)
- Batch processing with detailed reports

**Supported formats:** PDF, DOCX, TXT, RTF, HTML, MD

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
   # Single document
   path_arg = "document.pdf"
   
   # Folder with documents
   path_arg = "/path/to/documents/"
   
   # Analysis options
   include_hashes = True
   detailed_analysis = True
   ```

4. **Run all cells to analyze**

## 📁 Output
- `filename_analysis.txt` with detailed report
- JSON format available for programmatic use
