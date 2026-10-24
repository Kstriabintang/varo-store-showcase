<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="img/varo-logo-light.webp">
  <img src="img/varo-logo.png" alt="Varo Store" width="140">
</picture>

# Varo Store

### A PPOB + game top-up store for a village in Riau: online shop, store kasir and owner panel in one system

<p>
<a href="https://kstriabintang.github.io/varo-store-showcase/"><img alt="Showcase" src="https://img.shields.io/badge/showcase-open%20the%20page-e9b444?style=for-the-badge&labelColor=2a1a2f"></a>
</p>

<p>
<img alt="Laravel 13" src="https://img.shields.io/badge/Laravel%2013-2a1a2f?style=flat-square&logo=laravel&logoColor=e9b444">
<img alt="PHP 8.5" src="https://img.shields.io/badge/PHP%208.5-2a1a2f?style=flat-square&logo=php&logoColor=e9b444">
<img alt="Vue 3" src="https://img.shields.io/badge/Vue%203-2a1a2f?style=flat-square&logo=vuedotjs&logoColor=e9b444">
<img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-2a1a2f?style=flat-square&logo=typescript&logoColor=e9b444">
<img alt="Tailwind CSS 4" src="https://img.shields.io/badge/Tailwind%204-2a1a2f?style=flat-square&logo=tailwindcss&logoColor=e9b444">
<img alt="MySQL" src="https://img.shields.io/badge/MySQL%20%C2%B7%20SQLite-2a1a2f?style=flat-square&logo=mysql&logoColor=e9b444">
</p>
<p>
<img alt="Tests" src="https://img.shields.io/badge/tests-1667%20backend%20%2B%208%20frontend-e9b444?style=flat-square&labelColor=3b1f47">
<img alt="Catalog" src="https://img.shields.io/badge/catalog-512%20products-e9b444?style=flat-square&labelColor=3b1f47">
<img alt="Audit" src="https://img.shields.io/badge/audit-hash%20chain-e9b444?style=flat-square&labelColor=3b1f47">
<img alt="Status" src="https://img.shields.io/badge/status-v4%20%C2%B7%20pre--launch-e9b444?style=flat-square&labelColor=3b1f47">
</p>

**A product of Ksatria Bintang Samudra** · Built for **PT Luxavero Teknologi Indonesia**

<img src="img/store-home-desktop.webp" alt="Varo Store home page" width="860">

</div>

> **This is the public showcase / portfolio repository.** It holds the one-page showcase (`index.html`, served by GitHub
> Pages) and its screenshots. **Source code is private**: the application lives in a private repository.
>
> All screenshots use seeded demo data: no real customers, orders or credentials appear in them.

---

## What Varo Store is

In Kempas, Indragiri Hilir, Riau, phone credit, electricity tokens, e-wallet top-ups and game diamonds are bought at a counter:
you walk in, say a number, pay cash. Monthly bills (electricity, water, health insurance, motorbike instalments) often mean a
trip to town. Varo Store puts all of that in one place, for two kinds of customers:

- **At the store** - a tablet kasir sells digital products, physical goods (SIM cards, accessories) and bills in one cart, paid
  in cash, by the store's QRIS or by bank transfer, with a printed 58/80 mm receipt.
- **Online** - customers order from their phone, pay the store's QRIS, staff confirm the payment, and the order is sent to the
  supplier automatically.

The owner sees every order, every rupiah in the cash drawer, the stock on the shelf and an audit trail of every staff action,
from a web panel and from a Telegram bot.

The catalogue currently holds **512 products**: phone credit and data for every Indonesian operator, e-wallets, 50 games with
official artwork, and 65 bill providers.

---

## Key features

### Online shop

- **Every category, one look** - credit, data, electricity tokens, e-wallets, game vouchers, bills. The operator is detected
  from the phone number; each game asks for its own account fields (User ID + Zone ID for Mobile Legends, and so on).
- **QRIS payment with a unique amount** - every order gets a few extra rupiah so the payment can be matched in the bank
  statement; a 30-minute countdown, then the page updates itself.
- **Order tracking** - order code from the receipt, or the list of orders placed from this device. Destination numbers are
  always masked on public pages.

### Bills

Electricity (postpaid), 30 water utilities, health and employment insurance, internet, postpaid mobile, cable TV, gas and
multifinance instalments. The bill is checked first; amount, fee and total are shown before paying. The number field is
named the way each biller names it (customer number for water, contract number for instalments, member NIK for employment
insurance).

### Store kasir (tablet)

- **One cart** for digital products, goods and bills; cash, store QRIS or bank transfer.
- **Barcode scanning** - a USB scanner types the code and presses Enter; exact matches go straight into the cart.
- **Round in-store prices** - the kasir charges whole thousands and never less than the online price.
- **Number check before money moves** - the destination number is shown in large digits for the customer to confirm.
- **Shifts and the cash drawer** - opening float, cash sales, refunds, cash in/out; closing a shift locks it.

### Owner panel

- **Summary** - what needs action first (payments waiting, refunds owed, unmatched payments, low stock), then today's numbers,
  a breakdown per business line and a 7-day chart.
- **Transactions** with a full timeline per order: created, paid, sent to the supplier, supplier answer, status checks.
- **Payment matching** - QRIS and transfer payments ticked off one by one against the bank statement.
- **Products & prices, store banners, stock, reports, users, settings.** Staff only see the menus and numbers their
  permissions allow; cost and profit never leave the server for staff without the reports permission.

### Stock

Physical goods with barcodes, low-stock thresholds, goods received, stock counts and write-offs. Sales at the kasir take items
off the shelf; a cancelled sale puts them back.

### Audit trail

Every staff action is stored as a hash chain. One button re-reads the whole chain and proves nothing was edited, deleted or
inserted; the latest hash is also sent to Telegram every night, outside the database.

### Telegram bot and reports

A management bot with a fixed keyboard: today's summary, this month, per business line, what needs action, supplier balance,
shift and cash, stock, and PDF reports. Automatic notifications for orders, refunds, stock, low balance and staff logins, a
daily summary at 21:00 and a monthly report on the 1st. Reports are also available in the panel, as CSV, and as PDF (monthly
report, internal price list, and a wall price list for the store in A4 or A3). Every transaction is mirrored to Google Sheets,
one tab per business line, with destination numbers masked and no customer contact data.

---

## Screens

**Online shop**

| Home (phone) | Game page | QRIS payment | Order done |
|:---:|:---:|:---:|:---:|
| <img src="img/store-home-phone.webp" width="190"> | <img src="img/store-game-mobile-legends-phone.webp" width="190"> | <img src="img/store-order-qris-phone.webp" width="190"> | <img src="img/store-order-success-phone.webp" width="190"> |

| Game vouchers | Mobile Legends | Waiting for QRIS |
|:---:|:---:|:---:|
| <img src="img/store-voucher-game-desktop.webp" width="300"> | <img src="img/store-game-mobile-legends-desktop.webp" width="300"> | <img src="img/store-order-qris-desktop.webp" width="300"> |

| Order done | Track an order | Track (phone) |
|:---:|:---:|:---:|
| <img src="img/store-order-success-desktop.webp" width="300"> | <img src="img/store-cek-pesanan-desktop.webp" width="300"> | <img src="img/store-cek-pesanan-phone.webp" width="160"> |

**Bills**

| Bill types | Water utility picker | Picker (phone) |
|:---:|:---:|:---:|
| <img src="img/store-tagihan-desktop.webp" width="300"> | <img src="img/store-tagihan-pdam-desktop.webp" width="300"> | <img src="img/store-tagihan-pdam-phone.webp" width="160"> |

**Store kasir (tablet)**

| Digital products | Goods by barcode | Bill at the kasir | 58 mm receipt |
|:---:|:---:|:---:|:---:|
| <img src="img/kasir-digital-cart.webp" width="250"> | <img src="img/kasir-barang-scan.webp" width="250"> | <img src="img/kasir-tagihan-pdam.webp" width="250"> | <img src="img/kasir-struk-58mm.webp" width="120"> |

**Owner panel**

| Needs action | Summary (staff view) | Transactions |
|:---:|:---:|:---:|
| <img src="img/panel-ringkasan.webp" width="300"> | <img src="img/panel-ringkasan-staf.webp" width="300"> | <img src="img/panel-transaksi-staf.webp" width="300"> |

| Order timeline | Payment matching | Store banners |
|:---:|:---:|:---:|
| <img src="img/panel-detail-pesanan.webp" width="300"> | <img src="img/panel-cocokkan-pembayaran.webp" width="300"> | <img src="img/panel-banner-toko.webp" width="300"> |

| Stock | Audit (hash chain) | Store settings |
|:---:|:---:|:---:|
| <img src="img/panel-stok-staf.webp" width="300"> | <img src="img/panel-audit.webp" width="300"> | <img src="img/panel-pengaturan-toko.webp" width="300"> |

| Wall price list (PDF) |
|:---:|
| <img src="img/pdf-daftar-harga-pajang.webp" width="240"> |

All screenshots come from an isolated copy of the application with seeded test data: no real customers, numbers or accounts.
The interface is in Bahasa Indonesia.

---

## Engineering highlights

**Money safety**

| | What | How |
|---|---|---|
| 1 | **No double orders** | The pay button, kasir checkout and stock movements send an idempotency key; a repeat returns the first result. Each order goes to the supplier exactly once with its own reference; an unclear result is only ever *checked*, never re-sent as a new purchase. |
| 2 | **Bill-token binding** | Checking a bill returns a token bound to that product and customer number, valid for that day. An order that tries to pay a different number with it is refused. A bill only counts as paid once the supplier returns a serial number. |
| 3 | **Locked shift close** | Closing a kasir shift is atomic and locks the drawer: a sale or refund that arrives after the cash was counted is refused or flagged as a refund owed, so the drawer always matches. |
| 4 | **Audit hash chain** | `hash = sha256(prev_hash . row)`; a single locked head row serialises writers and a unique index on `prev_hash` rejects forks. A verifier re-reads the chain on demand, and a nightly anchor sends the latest hash to Telegram. |
| 5 | **Held, not failed** | When the supplier refuses for a reason on the store's side (balance, configuration), the order is held and retried automatically instead of being failed; a late success on an order already failed is never applied automatically, it goes to the owner for review. |
| 6 | **Test orders stay test orders** | Each order remembers the supplier mode it was created in; orders from development mode are never sent once the store is live, and production mode is refused on any machine that is not the production server. |

**Speed** - the public catalogue, the kasir catalogue and the dashboard are built once a minute and rebuilt as soon as a
price or product changes. Median API times went from 0.45 s to **0.014 s** (catalogue), 0.43 s to **0.019 s** (kasir) and
0.31 s to **0.094 s** (dashboard): all three under 0.2 s.

**Permissions enforced by the server** - per-person permissions (kasir, payment confirmation, reports, stock, deposit, cost at
the kasir). The router hides what a person may not open and every API route checks again; cost and profit fields are simply not
in the response for staff without the reports permission.

**Tested** - **1667 automated backend tests** (supplier connection with a fake HTTP client, pricing, money flows, bills,
permissions, stock, audit chain, Telegram, Google Sheets, PDFs) plus 8 frontend unit tests. A responsive sweep checks every
page at 390, 820, 1024 and 1366 px for sideways scroll, clipped text, small touch targets and broken images.

---

## Architecture

```mermaid
flowchart LR
  subgraph SPA["Vue 3 SPA (one build)"]
    S["Online shop"]
    K["Store kasir"]
    P["Owner and staff panel"]
  end
  S --> API
  K --> API
  P --> API
  API["Laravel 13 API<br/>/api/v1, Sanctum cookie"] --> DB[("MySQL 8 / MariaDB<br/>SQLite in development")]
  API --> Q[["Database queue"]]
  SCH["Scheduler"] --> Q
  Q --> W1["Worker: orders"]
  Q --> W2["Worker: notifications<br/>Telegram, email, Sheets, PDF"]
  W1 <--> SUP["PPOB supplier API"]
  SUP -- "signed webhook" --> API
  W2 --> TG["Telegram Bot API"]
  W2 --> GS["Google Sheets"]
```

Two queues keep paid orders from ever waiting behind slow jobs (PDF rendering, Sheets, Telegram). The supplier sits behind a
single gateway that owns the mode, the per-minute call budget, a circuit breaker and the hold-and-retry rules.

## Tech stack

**Backend** PHP 8.5 · Laravel 13 · Sanctum · DomPDF · database queue · PHPUnit (1667 tests) · MySQL 8 / MariaDB · SQLite (dev)
**Frontend** Vue 3.5 · Vue Router 4 · TypeScript · Vite 8 · Tailwind CSS 4 · lucide icons · Plus Jakarta Sans
**Integrations** PPOB supplier API (DigiFlazz) · Telegram Bot API · Google Apps Script (Sheets) · SMTP receipts
**Server** Ubuntu · Nginx · PHP-FPM · Supervisor · cron · Let's Encrypt
**Tooling** Playwright (isolated screenshot environment, responsive sweep) · Laravel Pint

---

## Status

| Area | Status |
|---|---|
| Online shop: all categories, QRIS payment, order tracking | ✅ done |
| Bills: 65 providers, check-then-pay, same-day token | ✅ done |
| Store kasir: digital + goods + bills, barcode, shifts, 58/80 mm receipts | ✅ done |
| Owner panel: summary, transactions, payment matching, products & prices, stock, banners, reports, users, settings | ✅ done |
| Audit hash chain with verifier and Telegram anchor | ✅ done |
| Telegram management bot, Google Sheets ledger, PDF reports | ✅ done |
| Move to a production server and go live | ⏳ next |

> **Honest note:** Varo Store is finished and tested but not yet live: the production server, the supplier agreement and the
> store's real QRIS are the remaining steps. There is no public demo.

---

## About this repository

| File | What it is |
|---|---|
| `index.html` | The one-page showcase (GitHub Pages): no build step, no JavaScript framework |
| `img/` | Product screenshots (`store-*`, `kasir-*`, `panel-*`, `pdf-*`) and the Varo Store logo |
| `.nojekyll` | Serve the files as they are |

<div align="center"><sub>Varo Store - a product of Ksatria Bintang Samudra · built for PT Luxavero Teknologi Indonesia · application source code is private</sub></div>
