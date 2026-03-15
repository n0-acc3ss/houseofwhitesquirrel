# 🐿️ บ้านกระรอกขาว — Online Menu

An elegant, mobile-friendly online menu for **บ้านกระรอกขาว** — Vietnamese, Isan & Thai café restaurant. Built as a zero-dependency single-file HTML application, deployed via Netlify.

---

## 📋 Project Structure

```
.
├── karokkaw-menu.html   # Main menu — single-file app (HTML + CSS + JS + logo)
├── _headers             # Netlify HTTP security headers
├── netlify.toml         # Netlify build & redirect configuration
└── README.md            # This file
```

---

## ✨ Features

- **10 category navigation** — all categories visible at a glance on first load
- **Search / filter** — live search across Thai and English item names
- **Bilingual** — Thai (default) ↔ English toggle
- **Add to order** — cart with running total
- **Special remarks** — one custom note per item (e.g. ไม่เผ็ด / not spicy)
- **Portion picker** — for multi-price items (e.g. ถ้วย / หม้อไฟ)
- **เรียกพนักงาน** — call staff button with table number field
- **Tap-to-call** — phone number opens dialler on mobile
- **No dependencies** — zero npm, zero build step, single `.html` file

---

## 🍜 Menu Categories

| # | Thai | English |
|---|------|---------|
| 1 | เมนูแนะนำอาหารเวียดนาม | Vietnamese Recommended |
| 2 | เมนูแนะนำอาหารไทยและอื่นๆ | Thai & Other Specials |
| 3 | ลาบ / ยำ | Laab & Spicy Salads |
| 4 | ทอดผัด | Stir-fry & Fried |
| 5 | ปลา | Fish Dishes |
| 6 | ปลาหมึกไข่ | Fresh Egg Squid |
| 7 | ต้มจืด / แกง | Soups & Curries |
| 8 | กาแฟ บ้านกระรอกขาว | Coffee |
| 9 | เครื่องดื่ม | Drinks |
| 10 | ของหวาน / ของทานเล่น | Snacks & Sweets |

---

## 🛠️ Updating the Menu

All menu data lives in a `const menuData = { ... }` object inside `karokkaw-menu.html`.

Each item follows this structure:
```js
{ id:'xx00', th:'ชื่อภาษาไทย', en:'English Name', price:'120' }

// Multi-price items — add a portion label:
{ id:'xx00', th:'ชาวนาว', en:'Lime Tea', price:'50 / 60', portion:'ร้อน / เย็น' }

// Items without a listed price (e.g. photo-only):
{ id:'xx00', th:'หมูย่างใบชะพลู', en:'Grilled Pork with Cha-Plu', price:'' }
```

To add a new category, add a `<div class="menu-section">` block in the HTML, a matching `.cat-card` in the grid, a `<div class="items-grid" id="grid-yourkey">` inside it, and a key in `menuData`.

---

## 📞 Restaurant Info

| | |
|---|---|
| **Name** | บ้านกระรอกขาว (Baan Krarok Khao) |
| **Tel** | 082 473 6114 |
| **Cuisine** | อาหารเวียดนาม / อีสาน / ไทย · เบียร์ · ไวน์ |
| **Café hours** | 9:00 – 21:00 |
| **Restaurant hours** | 11:00 – 21:00 |
| **Hashtag** | #แหนมเมืองบ้านตาคลี |

---

## 📄 License

This project is proprietary. All rights
reserved by บ้านกระรอกขาว.
