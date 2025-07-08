# 📄 Document Scraper

This script (`document_scraper.py`) is designed to scrape documents (PDF, DOCX, ZIP, etc.) from structured category-based websites with pagination.

## ✅ Features

- Crawls category pages with pagination
- Extracts downloadable documents (.pdf, .doc, .zip, etc.)
- Saves files locally in a structured folder
- Logs metadata (category, file name, file URL) into `ekdd_metadata.csv`

## 🛠️ Usage

1. Open the script and set:
   - `BASE_URL` to your target website's base page
   - `DOWNLOAD_FOLDER` to the path where files should be saved

2. Run the script:
```bash
python document_scraper.py
```

3. Scraped documents will be downloaded in folders by category, and metadata will be saved in `ekdd_metadata.csv`.

## ⚠️ Notes

- Make sure the website allows scraping (check its `robots.txt`).
- Customize the category keywords if needed.
- Avoid sending too many requests too quickly to prevent blocking.

---

