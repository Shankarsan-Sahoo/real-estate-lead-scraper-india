# 🏢 Hyderabad Real Estate Lead Scraper

Automatically discovers real estate company leads in Hyderabad from Google Maps.

---

## 📋 Output Columns

| Column | Description |
|---|---|
| **Company Name** | Real company name from Google Maps |
| **Phone** | Contact number (blank if not listed on Maps) |
| **Website** | Official company website |
| **Source** | Google Maps |
| **Phone Found** | Yes / No |

---

## 🔍 Source

**Google Maps** via Selenium

- Searches multiple queries (`real estate builders Hyderabad`, `property developers Hyderabad`, etc.)
- Collects all place URLs from search results
- Navigates to each place page directly for a clean DOM
- Extracts company name, phone, and website from each listing

---

## ✅ Rules

- Company Name + Website = **required** (record skipped if missing)
- Phone = **saved if found**, blank if not listed on Maps
- Blacklisted domains (JustDial, LinkedIn, Reddit, 99acres etc.) are filtered out
- Duplicates removed across all queries

---

## 🚀 Setup

### Requirements
- Python 3.8+
- Google Chrome
- ChromeDriver matching your Chrome version → https://chromedriver.chromium.org/downloads

### Install dependencies

```bash
pip install selenium requests beautifulsoup4 pandas openpyxl
```

---

## ▶️ Run

```bash
python hyderabad_realestate_leads.py
```

Chrome will open automatically and start scraping. To run without a browser window:

```python
# In the script change:
driver = build_driver(headless=True)
```

---

## 📊 Expected Results

- ~170 unique place URLs collected across 5 search queries
- ~130 leads saved (companies that have a website listed on Maps)
- ~110 with phone number, ~20 website only

---

## 📁 Output

File: `hyderabad_realestate_leads.xlsx`

| Row Color | Meaning |
|---|---|
| 🟢 Green | Has phone number |
| 🟡 Yellow | Website only — no phone listed on Maps |

---

## ➕ Get More Leads

Add more search queries in the script:

```python
GMAPS_QUERIES = [
    "real estate builders Hyderabad",
    "property developers Hyderabad",
    "real estate companies Hyderabad",
    "residential builders Hyderabad",
    "construction companies Hyderabad",
    # Add more below
    "gated community builders Hyderabad",
    "villa developers Hyderabad",
    "plot developers Hyderabad",
]
```

Each new query adds ~50-60 more unique companies.

---

## ⚠️ Notes

- Do **not** push the `.xlsx` output file to GitHub
- For personal/research use only
- Business phone numbers scraped are publicly listed on Google Maps

---

## Keywords
google maps scraper python, real estate leads scraper, selenium google maps scraper, india lead generation tool, business leads scraper
