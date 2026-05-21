---

# 🎰 5050 Lottery Data Tracker

This Python project automatically scrapes daily lottery prize values from three websites and stores them in an Excel file using **openpyxl**.

---

## 📌 Features

* Scrapes daily lottery jackpot values from:

  * HSN 50/50 Lottery
  * Split the Pot
  * Thunder Bay 50/50 lottery
* Stores data in an Excel file
* Automatically organizes data by month (sheet per month)
* Adds date for each entry
* Appends new data every day

---

## 🧰 Tech Stack

* Python
* BeautifulSoup
* requests
* openpyxl
* datetime

---

## 📁 Excel Structure

Each month has its own sheet:

| Date       | HSN Lottery | SplitThePot | ThunderBay5050 |
| ---------- | ----------- | ----------- | -------------- |
| 2026-05-21 | $xxx,xxx    | $xxx,xxx    | $xxx,xxx       |

---

## 🚀 How It Works

1. Opens existing Excel file:
   `5050 lottery data.xlsx`

2. Checks if a sheet for the current month exists:

   * If not → creates one (e.g., "May", "Jun")
   * If yes → uses existing sheet

3. Scrapes data from all websites

4. Adds a new row with:

   * Current date
   * HSN lottery value
   * SplitThePot value
   * ThunderBay5050 value

5. Saves the Excel file

---

## ▶️ How to Run Manually

```bash
python your_script.py
```

---

## ⏰ Run Automatically Every Day (9 AM)

Use **cron (recommended for macOS/Linux)**

### Step 1: Open cron editor

```bash
crontab -e
```

### Step 2: Add this line

```bash
0 9 * * * /usr/bin/python3 /path/to/your_script.py
```

---

## 🧠 What this means

```
0 9 * * *
```

* 0 → minute
* 9 → hour (9 AM)
* * → every day/month/weekday

So it runs:
👉 **Every day at 9:00 AM automatically**

---

## ⚠️ Important Notes

* Your Mac/PC must be ON at 9 AM
* Use correct Python path (`which python3`)
* Make sure `5050 lottery data.xlsx` exists before running

---

## 🛠️ Install Dependencies

```bash
pip install requests beautifulsoup4 openpyxl lxml
```

---