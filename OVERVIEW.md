# Project Overview

## Purpose
A professional website for Sri A to Z Mega Shopping Mall, Suryapet, that lets customers browse everything the mall sells and order through WhatsApp.

## Sections of the page
1. **Header:** logo (click to refresh), category search, Profile menu, phone, WhatsApp, Instagram, dark mode, and a link bar (Home, Shop, About us, Contact, Why only us, Reviews).
2. **Home:** hero banner with the store photo, and a "Popular" area with sample items from every category.
3. **Shop:** a scrolling category strip, a sub-section sidebar and an item grid for five categories:
   - Home Appliances
   - Toys & Games
   - School Essentials
   - Decor Items
   - Plastic Items
4. **About us:** the shop story, years of service and key facts.
5. **Contact and Address:** phone, WhatsApp, address, opening hours, payments (all cards accepted, Bajaj Finserv EMI), Google Maps link and WhatsApp group.
6. **Why only us:** reasons to shop here and a scrolling strip of partner brand logos.
7. **Reviews:** customers can leave a star rating, a written review and a video review.
8. **Footer:** quick links and contact details.

## Customer features
- **Search:** type an item name, see the A to Z logo loader, and jump to the matching item.
- **Item details:** clicking an item opens a large photo view with an Order now button and a note that the shop can transport all over the world.
- **Order now:** opens WhatsApp with the item name already filled in, plus the customer's saved details.
- **Sign up before ordering:** name, phone, email and postal address are asked once and remembered on the device.
- **Profile menu:** Your Account, Your Orders and Your Wish List.
- **Wishlist:** heart button on every item. Logged-out visitors are asked to log in first.
- **Dark mode** and a light default theme.
- **Loader:** the A to Z logo shows while the page loads and when navigating.
- **Responsive layout** for phones, tablets and desktops.

## How it is built
- One self-contained `index.html` (HTML, CSS and JavaScript together). No framework and no build step.
- The catalogue is a JavaScript data list (`CATALOG`), so adding an item means adding one line.
- All product photos and logos are embedded in the file as data, so the site works from any host.
- Visitor data (profile, wishlist, orders, reviews) uses the browser's `localStorage` and `IndexedDB`.

## Limits and ideas for later
- No server: the shop does not receive accounts, orders or reviews except through WhatsApp messages.
- Next steps if wanted: a small backend or Firebase for real customer accounts, order tracking and shared reviews; a custom domain such as `atozmegamall.in`; a price list; more product photos.
