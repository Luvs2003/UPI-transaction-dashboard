# UPI Transaction Dashboard

An interactive Power BI dashboard analyzing 20,000 UPI (Unified Payments Interface) transactions across Indian cities, built to explore transaction behavior, balance trends, and merchant/payment-method patterns.

---

## 📌 Project Overview

This project visualizes UPI transaction data to help identify spending patterns, transaction trends, and customer behavior across banks, cities, devices, and merchants. The dashboard spans **two pages** with **synced slicers** and **bookmark-driven chart toggles**, giving users a smooth, app-like way to explore the data.
<img width="1920" height="1020" alt="Screenshot 2026-07-29 181244" src="https://github.com/user-attachments/assets/114d7e83-91de-4afb-ba4a-1b0a1d642f49" />



---

## 🗂️ Data Model

**Table:** `UPI transaction` — 20,000 rows

| Field | Description |
|---|---|
| TransactionID | Unique transaction identifier |
| TransactionDate / TransactionTime | Date and time of transaction |
| Amount | Transaction amount |
| RemainingBalance | Account balance after the transaction |
| BankNameSent / BankNameReceived | Sender and receiver banks |
| City | Customer's city |
| CustomerAccountNumber / MerchantAccountNumber | Account identifiers |
| CustomerAge / Age Groups | Customer demographics |
| Gender | Customer gender |
| DeviceType | Device used (Mobile, Laptop, etc.) |
| MerchantName | Merchant receiving payment (Amazon, Flipkart, IRCTC, Swiggy, Zomato) |
| PaymentMethod / PaymentMode | Mode of payment (Phone Number, QR Code, UPI ID) |
| Purpose | Reason for transaction |
| TransactionType | Type of transaction (e.g., Transfer) |
| Status | Success/Failure of transaction |
| Currency | Transaction currency |
<img width="1920" height="1020" alt="Screenshot 2026-07-29 181219" src="https://github.com/user-attachments/assets/110f4f30-b061-44a0-9ca3-7514fd0af21e" />


---

## 📊 Dashboard Structure

### Page 1 — Transaction & Balance Trends
- **Filters/Slicers:** BankNameSent, BankNameReceived, City, DeviceType, Gender, Age Groups, MerchantName, PaymentMethod, Purpose, TransactionType
- **Main Visual:** Monthly trend chart (Jan–Dec 2024) with **4 toggle views** controlled via bookmarks:
  - Line Chart – Amounts
  - Column Chart – Amounts
  - Line Chart – Balance
  - Column Chart – Balance

### Page 2 — City x Currency x Month Matrix
- A matrix breaking down **Amount** and **RemainingBalance** by **City, Currency, and Month**, with conditional-formatting trend icons (▲ up, ▼ down, ● stable) and data bars for quick visual scanning.
- Same filter panel as Page 1, kept in sync via **Sync Slicers**.

### Interactivity Features
- **Synced Slicers:** All 10 filters behave identically across both pages.
- **Bookmarks:** Power the 4-way chart toggle (Line/Column × Amount/Balance) on Page 1 without needing separate pages.
- <img width="1920" height="1020" alt="Screenshot 2026-07-29 181414" src="https://github.com/user-attachments/assets/94051b95-24d5-4101-a49c-0df6478e27eb" />


---

## 🔍 Key Findings

- **Seasonal spending pattern:** Transaction volumes peak in **May and October**, dipping in **March/April and August** — useful for planning campaigns or staffing around demand cycles.
- **Stable merchant performance:** Amazon transactions show consistent customer balances year-round, signaling low payment friction with top merchants.
- **High-value niche channel:** Phone-number-based payments are used less often but carry **much higher transaction values**, flagging a segment worth targeting for premium services.
- **Mobile-first behavior:** The large majority of transactions happen on **mobile devices**, reinforcing the need for mobile-optimized payment experiences.
- **Clean, reliable dataset:** Near-zero duplication in balance records supports confident, trustworthy reporting.
- <img width="1920" height="1020" alt="Screenshot 2026-07-29 185517" src="https://github.com/user-attachments/assets/a397fd92-d6b4-4c2b-aa77-0e90504c5413" />


---

## 🛠️ Tools Used
- **Power BI Desktop** (Data Modeling, DAX, Bookmarks, Sync Slicers, Conditional Formatting)
- Source file: `UPI_Transaction_Dashboard.pbix`
