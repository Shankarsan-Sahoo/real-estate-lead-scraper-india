# 🏢 Google Maps Real Estate Lead Scraper (Python | India)

🔥 Scrapes 100+ real estate leads (with phone & website) in minutes from Google Maps

Automatically discovers **real estate companies in Hyderabad** using Google Maps and enriches data from multiple sources.

---

## 🚀 Features

* ✅ Scrapes real estate companies from **Google Maps**
* ✅ Extracts:

  * Company Name
  * Phone Number
  * Website
* ✅ Multi-source enrichment:

  * Google Maps
  * Sulekha
  * TradeIndia
* ✅ Smart phone validation (India-specific)
* ✅ Filters out spam/directory websites (JustDial, 99acres, etc.)
* ✅ Removes duplicates across all sources
* ✅ Excel output with color formatting
* ✅ Handles dynamic pages (no stale element issues)

---

## ⚙️ How It Works

1. Collects Google Maps place URLs using multiple search queries
2. Navigates directly to each place page (avoids stale DOM issues)
3. Extracts:

   * Company name
   * Website (filtered)
   * Phone number (validated)
4. Enriches additional leads from:

   * Sulekha
   * TradeIndia
5. Deduplicates results across all sources
6. Saves structured data into Excel

---

## 📋 Output Format

| Column       | Description                        |
| ------------ | ---------------------------------- |
| Company Name | Business name from source          |
| Phone        | Contact number (if available)      |
| Website      | Official company website           |
| Source       | Google Maps / Sulekha / TradeIndia |
| Phone Found  | Yes / No                           |

---

## 📊 Output File

```
hyderabad_realestate_leads.xlsx
```

### Row Colors:

* 🟢 **Green** → Has phone number
* 🟡 **Yellow** → Website only

---


## 🛠️ Setup

### Requirements

* Python 3.8+
* Google Chrome
* ChromeDriver (matching your Chrome version)

👉 Download: https://chromedriver.chromium.org/downloads

---

### Install Dependencies

```bash
pip install selenium requests beautifulsoup4 pandas openpyxl
```

---

## ▶️ Run

```bash
python hyderabad_realestate_scraper.py
```

To run in headless mode:

```python
driver = build_driver(headless=True)
```

---

## 📈 Expected Results

* ~170 unique Google Maps listings collected
* ~130 valid leads (with website)
* ~110 with phone number
* ~20 website only

---

## ➕ Get More Leads

Add more queries inside the script:

```python
GMAPS_QUERIES = [
    "real estate builders Hyderabad",
    "property developers Hyderabad",
    "real estate companies Hyderabad",
    "residential builders Hyderabad",
    "construction companies Hyderabad",
    "villa developers Hyderabad",
    "plot developers Hyderabad",
]
```

Each query adds ~50–60 more companies.

---

## ⚠️ Notes

* Do NOT upload generated `.xlsx` file to GitHub
* For **personal / research use only**
* Data is scraped from publicly available sources

---

## 💡 Use Cases

* Real estate lead generation
* Sales prospecting
* Market research
* Local business intelligence

---

## 🧠 Problem Solved

Manually collecting real estate leads from Google Maps is slow and inefficient.

This tool automates:

* Data discovery
* Contact extraction
* Lead structuring

👉 Saving hours of manual work.

---

## 🏷️ Keywords

google maps scraper python, real estate leads scraper, selenium scraper india, business leads extraction, google maps automation, lead generation python

---

## ⭐ Support

If this project helps you:

👉 ⭐ Star this repository
👉 Share it with others

---

## 👨‍💻 Author

**Shankarsan Sahoo**
Full Stack Python Developer

---

## 📜 License

This project is for educational and research purposes.
