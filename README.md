# India-Stocks-2281-2310-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2281 to 2310)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2281-2310-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2281 to 2310)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2281 | `STANLEY` | Stanley Lifestyles Limited | `STANLEY.NS` |
| 2282 | `STAR` | Strides Pharma Science Limited | `STAR.NS` |
| 2283 | `STARCEMENT` | Star Cement Limited | `STARCEMENT.NS` |
| 2284 | `STARPAPER` | Star Paper Mills Limited | `STARPAPER.NS` |
| 2285 | `STARTECK` | Starteck Finance Limited | `STARTECK.NS` |
| 2286 | `STCINDIA` | The State Trading Corporation of India Limited | `STCINDIA.NS` |
| 2287 | `STEAMHOUSE` | Steamhouse India Limited | `STEAMHOUSE.NS` |
| 2288 | `STEELCAS` | Steelcast Limited | `STEELCAS.NS` |
| 2289 | `STEELCITY` | Steel City Securities Limited | `STEELCITY.NS` |
| 2290 | `STEELXIND` | STEEL EXCHANGE INDIA LIMITED | `STEELXIND.NS` |
| 2291 | `STEL` | Stel Holdings Limited | `STEL.NS` |
| 2292 | `STERTOOLS` | Sterling Tools Limited | `STERTOOLS.NS` |
| 2293 | `STLNETWORK` | STL Networks Limited | `STLNETWORK.NS` |
| 2294 | `STLSTRINF` | Steel Strips Infrastructures Limited | `STLSTRINF.NS` |
| 2295 | `STOVEKRAFT` | Stove Kraft Limited | `STOVEKRAFT.NS` |
| 2296 | `STUDDS` | Studds Accessories Limited | `STUDDS.NS` |
| 2297 | `STYL` | Seshaasai Technologies Limited | `STYL.NS` |
| 2298 | `STYLAMIND` | Stylam Industries Limited | `STYLAMIND.NS` |
| 2299 | `STYLEBAAZA` | Baazar Style Retail Limited | `STYLEBAAZA.NS` |
| 2300 | `STYRENIX` | Styrenix Performance Materials Limited | `STYRENIX.NS` |
| 2301 | `SUBEXLTD` | Subex Limited | `SUBEXLTD.NS` |
| 2302 | `SUBROS` | Subros Limited | `SUBROS.NS` |
| 2303 | `SUDARCOLOR` | Sudarshan Colorants India Limited | `SUDARCOLOR.NS` |
| 2304 | `SUDARSCHEM` | Sudarshan Chemical Industries Limited | `SUDARSCHEM.NS` |
| 2305 | `SUDARSHAN` | Sudarshan Pharma Industries Limited | `SUDARSHAN.NS` |
| 2306 | `SUDEEPPHRM` | Sudeep Pharma Limited | `SUDEEPPHRM.NS` |
| 2307 | `SUKHJITS` | Sukhjit Starch & Chemicals Limited | `SUKHJITS.NS` |
| 2308 | `SULA` | Sula Vineyards Limited | `SULA.NS` |
| 2309 | `SUMEDHA` | Sumedha Fiscal Services Limited | `SUMEDHA.NS` |
| 2310 | `SUMEETINDS` | Sumeet Industries Limited | `SUMEETINDS.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream STANLEY 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2281-2310-Historical-Data/main/STANLEY/1m/2026/10/STANLEY_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
