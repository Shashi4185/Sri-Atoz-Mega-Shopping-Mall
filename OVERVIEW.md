# Project Overview

## Purpose
A professional website for **Sri A to Z Mega Shopping Mall**, Suryapet (since 1995). Customers browse everything the mall sells and place orders through WhatsApp. The owner can see customer activity in a private dashboard.

Live site: https://atozmegashoppingmall.com/

## Sections of the page
1. **Header:** logo, search bar, profile menu, phone, WhatsApp, Instagram, dark mode, and a link bar (Home, Shop, About us, Contact, Why only us, Reviews).
2. **Home:** hero banner with the store photo and a "Popular" area with sample items from every category.
3. **Shop:** category strip, sub-section sidebar and an item grid.
4. **About us:** the shop story, years of service and key facts.
5. **Contact and Address:** phone, WhatsApp, address, payments (all cards accepted, Bajaj Finserv EMI), Google Maps link and WhatsApp group.
6. **Why only us:** reasons to shop here and a scrolling strip of partner brand logos.
7. **Reviews:** customers can leave a star rating and a written review.
8. **Footer:** quick links, contact details and the Privacy Policy link.

## Catalogue (195 items, each with a photo)
| Category | Sub-sections | Items |
|----------|--------------|-------|
| Home Appliances | Kitchenware & Appliances, Table & Ceiling Fans, Water Heaters & Geysers, Iron Boxes, Home Safes & Lockers | 115 |
| Toys & Games | Toys, Indoor Games, Cricket, Outdoor Sports | 22 |
| School Essentials | Tiffins & Bottles, Pouches & Bags | 11 |
| Decor Items | Wall Decor, Lights & Candles, Showpieces & Vases, Home Furnishing | 21 |
| Plastic Items | Storage Containers, Buckets & Tubs, Kitchen & Dining, Chairs & Tables, Household Basics | 26 |

New arrivals carry a "New" tag (for example the Godrej MYST Small Book Locker).

## Customer features
- **Search:** type an item name, see the A to Z logo loader, and jump to the matching item.
- **Item details:** clicking an item opens a large photo view with an Order now button.
- **Sign-up:** name, mobile number and postal address are needed before ordering. A profile menu shows the saved details and a logout option.
- **Order now:** opens WhatsApp (9578529529) with the item name and the customer's saved details already filled in.
- **Wishlist:** heart icon on every item.
- **Themes:** light and dark mode.
- **Mobile:** works on phones, tablets and desktops, including iPhone Safari.

## Customer activity tracking (Firebase)
- Powered by Google Firebase (free Spark plan): Authentication and Cloud Firestore, Mumbai region.
- Records: sign-up details (name, mobile number, address), login and logout times, searches, items viewed, wishlist changes and Order now taps.
- Collections: `events`, `sessions`, `customers`.
- Security rules allow only the owner's Google account to read data. Customers can only write their own records.
- The Firebase web keys in `config.js` are public identifiers, not secrets.
- Tracking switches on only when `config.js` is filled in.

## Owner dashboard
A private page, not linked from the site, shows:
- total customers signed up, logins and logouts
- most viewed products and who viewed them
- customer list with name, mobile number and address
- login/logout times, repeated picks and a full activity log
- CSV export

Access needs the owner's Google login. Anyone else sees a "404 not found" page and no data.

## Files
| File | Purpose |
|------|---------|
| `index.html` | The website |
| `*.jpg` | Product photos |
| `config.js` | Firebase settings |
| `privacy.html` | Privacy Policy |
| `404.html` | Page for wrong links |
| `favicon.ico`, `favicon-192.png`, `apple-touch-icon.png` | Tab and home-screen icons |
| `README.md`, `OVERVIEW.md` | Documentation |

## How to change things
- **Add or change an item:** edit the `CATALOG` list inside `index.html`. Each line is `Item name|short note|new` (the last part is optional). Add a matching photo.
- **Shop details** (phone, address, WhatsApp): edit the `SHOP` block in `index.html`.
- **Partner brands:** edit the `BRANDS` list.
- Commit the change on GitHub; the live site updates in 1-2 minutes.

## Still to do
- Buy a domain and connect it to GitHub Pages (add a `CNAME` file).
- Shop email is set in the `SHOP` block in `index.html` (sales, support and info all use it).
