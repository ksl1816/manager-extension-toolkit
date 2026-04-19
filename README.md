# Manager.io — Prompt Builder

> **Build custom Manager.io extensions in minutes — no coding required.**  
> Explore any API endpoint, inspect its data, and generate a complete AI prompt that produces a fully working extension.

![Version](https://img.shields.io/badge/version-1.0-blue)
![Platform](https://img.shields.io/badge/platform-Manager.io-orange)
![Type](https://img.shields.io/badge/type-Single%20HTML%20File-brightgreen)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

## What It Does

The **Manager.io Developer Toolkit** is a single-file extension that runs inside Manager.io. It bridges the gap between the Manager.io API and anyone who wants to build a custom extension — without needing to know the API structure, pagination rules, or how the postMessage bridge works.

**The full workflow in five steps:**

1. **Load** any Manager.io API endpoint — one click or type it in
2. **Inspect** the live JSON response — see every field, its type, and a sample value
3. **Select** the fields your extension needs using the sidebar
4. **Generate** a complete, structured AI prompt via the built-in AI Syntax Builder
5. **Paste** the prompt into Claude, ChatGPT, or Gemini → receive a working `.html` extension

---

## Features

| | Feature | Description |
|---|---|---|
| 🔍 | **API Explorer** | Browse any `/api4/` endpoint with full JSON syntax highlighting |
| ⚡ | **Quick Endpoints** | One-click shortcuts for customers, invoices, payments, inventory, employees, reports, and more |
| ⬇ | **Load All Records** | Automatically follows all pagination tokens — Manager.io caps responses at 50 records per call; this tool fetches everything |
| 🗂 | **Schema Inspector** | Left sidebar shows every field path, data type (str / num / bool / arr / obj / UUID), and a live sample value |
| 📋 | **Context Buffer** | Save responses from multiple endpoints and combine them in a single prompt |
| 🤖 | **AI Syntax Builder** | 5-step wizard — pick a template, describe your goal, select fields, choose a style, generate the prompt |
| 🎨 | **Style Themes** | Generated extensions support Dark, Light, and Minimal themes |
| 📖 | **Built-in Guide** | "How to Use" button in the toolbar — full step-by-step guide without leaving the extension |
| ⎘ | **Copy / Download** | Copy the prompt to clipboard or download an `.html` skeleton directly |

---

## Quick Start

### 1. Install

Add `index.html` as a Manager.io extension:

```
Manager.io → Settings → Extensions → Add New Extension → 
```

Paste the below URL
```
https://ksl1816.github.io/manager-extension-toolkit/
```

### 2. Load an Endpoint

Click any quick button (e.g. **sales invoices**) or type an endpoint name and press Enter:

```
batch-sales-invoice
batch-customer
aged-receivables
profit-and-loss-statement
```

Click **⬇ Load All** to fetch every record across all pages.

### 3. Select Fields

Use the left sidebar to tick the fields your extension needs. Click **Values only** to skip parent objects and keep only usable data fields.

### 4. Open the AI Syntax Builder

Click the floating **⎘ AI Context Buffer** button → switch to **AI Syntax Builder** tab → fill in the 5 steps → click **⚡ Generate**.

### 5. Paste into an AI and Install

Copy the generated prompt → paste into Claude, ChatGPT, or Gemini → save the returned HTML → upload as a new Manager.io extension.

> 📖 Click the **"How to Use"** button inside the extension for the full built-in guide.

---

## Supported Endpoints

**Lists**
`batch-customer` · `batch-supplier` · `batch-sales-invoice` · `batch-purchase-invoice` · `batch-receipt` · `batch-payment` · `batch-inventory-item` · `batch-employee` · `batch-bank-or-cash-account` · `batch-journal-entry`

**Summaries**
`batch-customer-summary` · `batch-supplier-summary` · `batch-sales-invoice-totals-by-customer`

**Reports**
`aged-receivables` · `aged-payables` · `trial-balance` · `profit-and-loss-statement` · `balance-sheet` · `general-ledger-transactions`

**Meta**
`businesses`

Any other valid `/api4/` endpoint can be typed manually.

---

## Extension Templates

When generating a prompt, choose from these presets or write your own goal:

| Template | Best for |
|---|---|
| 📊 Dashboard | Summary cards + key metrics at a glance |
| 📋 Data Table | Searchable, sortable list of records |
| 🔢 KPI Cards | Large highlight numbers |
| 📈 Chart | Bar, line, or pie charts |
| 🔍 Search / Filter | Find and filter specific records |
| ✏️ Create / Edit Form | Data entry forms |
| ⬇️ CSV Export | Download data as a spreadsheet |
| ✨ Custom | Describe anything in plain English |

---

## File Structure

```
manager-developer-toolkit/
├── indexfinal.html     ← The complete toolkit (single file, zero dependencies)
└── README.md           ← This file
```

---

## Technical Notes

- **Zero dependencies** — pure HTML, CSS, and vanilla JavaScript
- **No server required** — works as a static file hosted anywhere
- **Secure** — all API calls go through Manager.io's `postMessage` bridge (same as all official extensions)
- **Pagination handled automatically** — follows `next_page_token`, `nextPageToken`, and `_links.next.href`
- **AI-agnostic** — the generated prompt works with Claude, ChatGPT, Gemini, or any LLM
- **Responsive** — sidebar collapses on small screens

---

## License

MIT — free to use, modify, and distribute.

---

## 👤 Author

**ksl1816** — [github.com/ksl1816](https://github.com/ksl1816)

*Contributions, bug reports, and feature suggestions are welcome — open an issue or pull request.*

*Built for the Manager.io developer and user community.*
