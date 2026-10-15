# Sri A to Z Mega Shopping Mall, Suryapet

A single-page website for **Sri A to Z Mega Shopping Mall**, Suryapet, Telangana (serving customers since 1995).
Customers can browse the catalogue, save items to a wishlist and send orders to the shop on WhatsApp.

**Live site:** `https://<your-username>.github.io/<repository-name>/`

## What is in this repository

| File | Purpose |
| --- | --- |
| `index.html` | The whole website: HTML, CSS, JavaScript, logo and all product photos in one file |
| `README.md` | This guide |
| `OVERVIEW.md` | Features and how the site works |

There is no build step and no dependencies. Fonts (Hanken Grotesk, Playfair Display) load from Google Fonts.

## Run it locally

- Double-click `index.html`, or
- In this folder run `python -m http.server 8000` and open http://localhost:8000

## Publish with GitHub Pages

1. Put `index.html` in the repository root. Keep the name in lowercase.
2. Go to **Settings, Pages**.
3. Under **Build and deployment** choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then save.
4. After about a minute the site is live at the address shown on that page.

If you use a subfolder of an existing repository, the site will be at `https://<your-username>.github.io/<repository>/<folder>/`.

## Change the shop details

Open `index.html` in a text editor and search for these names near the start of the script:

| Name | What it controls |
| --- | --- |
| `SHOP` | Phone, address, opening hours, email |
| `ORDER_PHONE` | WhatsApp number that receives orders (country code first, no plus sign) |
| `INSTAGRAM` | Instagram username |
| `WA_GROUP` | WhatsApp group link |
| `CATALOG` | Categories, sub-sections and items (`"Item name|size or detail"`) |
| `PHOTOS` and `PHOTO_OF` | Product photos and which item uses which photo |

The phone number in the header popup and call link (`88853 85043`) also appears in the HTML near the top of the page. Search for `8885385043` to change it everywhere.

## Good to know

- Orders are sent through WhatsApp. There is no server or payment processing.
- Sign-up details, wishlist and order history are stored only in the visitor's own browser (`localStorage`). They are not shared between devices and the shop cannot see them except in the WhatsApp order message.
- Item names, sizes and floor numbers are sample data and should be checked before launch.


## Important: upload the `images` folder too
`index.html` is now small (about 130 KB) and loads product photos from the `images/` folder. Upload **index.html and the whole images folder** to GitHub (drag the folder into "Add file → Upload files"). If `images/` is missing, photos will not show. This makes the site open fast on iPhones.
