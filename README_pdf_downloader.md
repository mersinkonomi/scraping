# 📄 Automated PDF Downloader with Selenium

This script automates the downloading of PDF files using a list of page URLs. It uses Selenium to navigate each page, submit a download form, and rename the downloaded PDF file based on the page title.

## ⚙️ Features

- Reads URLs from a CSV file
- Navigates to each # page using Chrome
- Detects and submits the PDF download form
- Renames the downloaded PDF based on the page title
- Skips already-downloaded files (if size is sufficient)
- Cleans up incomplete `.crdownload` files

---

## 🔧 Configuration

Before running, configure the following in the script:

### Set paths:
```python
download_dir = "/path/to/save/pdfs"
csv_path = "/path/to/urls.csv"
```

### CSV structure:
Your CSV should have a column called `#_page_url`:
```csv
#_page_url
https://example.com/page1
https://example.com/page2
...
```

### ChromeDriver:
Update the path to your ChromeDriver:
```python
driver = webdriver.Chrome(service=Service("/path/to/chromedriver"), options=options)
```

> 💡 Ensure ChromeDriver matches your installed Chrome version.

---

## ▶️ How to Run

1. Install the dependencies:
```bash
pip install selenium
```

2. Run the script:
```bash
python pdf_downloader_cleaned.py
```

---

## 📝 Notes

- The script is not headless by default so you can see what's happening.
- It waits ~15 seconds after each download to avoid rate-limiting.
- If the downloaded file is below 10 KB, it assumes it failed and reattempts.
- Downloaded files are renamed based on the page’s `<h2 class='page-header'>` title.

---

## 🛑 Disclaimer

Use this script responsibly. Ensure that you have permission to download content from the source website and comply with their Terms of Service.
