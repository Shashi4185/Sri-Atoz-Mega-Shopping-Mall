# Database setup (Firebase, free plan)

What it saves: customer details, login time, logout / last-seen time, every item a customer views, wishlists, order-now clicks and searches. You see it all on `admin.html`.

## 1. Create the project (10 minutes)
1. Go to https://console.firebase.google.com and sign in with your Google account.
2. **Add project** → name it `atoz-mall` → continue (Google Analytics not needed).
3. **Build → Firestore Database → Create database** → choose a region near India (`asia-south1`, Mumbai) → **Production mode**.
4. **Build → Authentication → Get started** → **Sign-in method**:
   - enable **Anonymous**
   - enable **Google**
5. **Authentication → Settings → Authorized domains** → Add your site domains: `<username>.github.io` and your own domain (for example `atozmegamall.in`).

## 2. Security rules
1. Firestore → **Rules** tab.
2. Open `firestore.rules`, replace `YOUR_EMAIL@gmail.com` with your own Google email, copy everything, paste into the Rules tab, **Publish**.
This makes sure customers can only add data, and only you can read it.

## 3. Connect the website
1. Project settings (gear icon) → **Your apps** → web icon `</>` → register app → copy the `firebaseConfig` values.
2. Open `config.js` and paste `apiKey`, `authDomain`, `projectId`, `appId`.
3. Upload `config.js` to GitHub (replace the old one). The Firebase apiKey is not a password, so it is fine to be public. The rules protect the data.

## 4. See the data
Open `https://your-site/admin.html` → Sign in with Google (the same email as in the rules).
Tabs: Top items, Repeated picks (same customer choosing the same item again and again), Customers, Login / exit times, Activity log. "Download CSV" exports the activity.

## Notes
- Free plan (Spark) is enough for a local shop's traffic. Check Firebase pricing for current limits.
- "Left at" is the last time the page was open (updated every 30 seconds). Exact logout time is saved when the customer taps Log out.
- Delete a customer's data on request from the Firebase console (Firestore → customers / events).
- Without keys in `config.js`, the website works normally and just does not save to the database.
