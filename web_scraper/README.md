# 🌐 Web Scraper & PDF Converter

Convert web pages to PDF documents! Features:
- Single page conversion
- Batch processing
- Website crawling with automatic link discovery
- Custom CSS styling for better PDF output
- Screenshot mode for full-page capture
- Headless browsing with JavaScript support

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
   # Single URL
   urls = ["https://example.com"]
   mode = "pdf"
   
   # Batch processing
   urls = ["https://site1.com", "https://site2.com"]
   
   # Website crawling
   crawl_mode = True
   max_pages = 10
   
   # Custom styling
   custom_css = "nav { display: none; }"
   ```

4. **Run all cells to convert**

## 📁 Output
- `domain_name_page.pdf` for each converted page
- Screenshots available in screenshot mode
