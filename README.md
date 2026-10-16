# Sri A to Z Mega Shopping Mall, Suryapet

A single-page website for **Sri A to Z Mega Shopping Mall**, Suryapet, Telangana (serving customers since 1995). Customers can browse the catalogue, save items to a wishlist, sign up, and send orders to the shop on WhatsApp.

**Live site:** https://shashi4185.github.io/Sri-Atoz-Mega-Shopping-Mall/

## Features
- 5 categories with 190+ products, each with a photo and detail popup
- Search, wishlist, reviews, light and dark themes
- Sign-up before ordering; "Order now" opens WhatsApp
- Works on phones, tablets and desktops (including iPhone Safari)
- Customer activity tracking with Firebase (login/logout times, items viewed), visible only to the owner
- Privacy Policy page and a custom 404 page

## Files in this repository
| File | Purpose |
|------|---------|
| `index.html` | The website (HTML, CSS and JavaScript) |
| `*.jpg` | Product photos used by the website |
| `config.js` | Firebase project settings (public web keys) |
| `privacy.html` | Privacy Policy |
| `404.html` | Page shown for wrong links |
| `favicon.ico`, `favicon-192.png`, `apple-touch-icon.png` | Browser tab and home-screen icons |
| `README.md` | This guide |

The owner dashboard is a separate private page and is not linked from the website.

## Run it locally
In this folder run `python -m http.server 8000` and open http://localhost:8000
(opening `index.html` by double-click also works, but customer tracking needs a web server).

## Deploying
Hosted on GitHub Pages: **Settings > Pages > Deploy from a branch > `main` / root**.
Every commit updates the live site in 1-2 minutes.

## Data and security
Customer data is stored in Google Firebase (Cloud Firestore). Security rules allow only the shop owner's Google account to read it. The Firebase web keys in `config.js` are public identifiers, not secrets.

## Contact
Besides More Super Market, MG Road, Vidyanagar / Manasa Nagar, Suryapet, Telangana 508213
Phone: +91 88853 85043
