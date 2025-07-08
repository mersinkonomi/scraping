Web Scraping Scripts
====================

This project contains various Python scripts for scraping data from websites using:

- Public APIs
- BeautifulSoup (for static HTML content)
- Selenium (for dynamic JavaScript-rendered pages)

Each script is located in its corresponding folder.

How to Run
----------

1. Install the required dependencies:
   pip install -r requirements.txt

2. Run the appropriate script depending on the target source:
   - API scraping:        python api/scrape_api.py
   - HTML scraping:       python html/scrape_html.py
   - Selenium scraping:   python selenium/scrape_selenium.py

Output
------

All extracted data is saved in the 'output/' folder in formats like .json, .txt, or .csv.

Notes
-----

- Make sure to install the correct WebDriver if using Selenium (e.g., ChromeDriver).
- Use responsibly and respect website terms of service.

Author
------

Mersin Konomi
