[README.md](https://github.com/user-attachments/files/27563717/README.md)
# Holiday Companion 🌴

A personal travel organiser for family holidays. Stores flights, accommodation, activities, payments, traveller details and emergency contacts — all in one place, available offline on your phone and synced to your computer via Google Sheets.

---

## What it does

- **Trip timeline** — everything in date order with a "Next up" card showing your next flight, check-in or activity
- **Smart Import** — paste a booking confirmation email or upload a PDF and Claude fills in all the details automatically
- **Money tracker** — track what's paid, what's due before travel, and what you'll pay on arrival, with a running total
- **Travellers** — store passport details for your whole family once; select who's coming on each trip
- **Emergency contacts** — local emergency numbers, hospital, hotel, British consulate and travel insurance — one tap to call, works offline
- **Documents** — upload PDFs and images stored on your device for offline access
- **Notes** — add notes as cards directly in your trip timeline on the right day
- **Google Sheets sync** — data syncs between your phone and computer automatically
- **Works offline** — all data available without signal once loaded

---

## Getting it on your phone

1. Open the app URL in **Safari** on iPhone
2. Tap the **Share** button → **Add to Home Screen**
3. Tap Add — it appears as an app icon on your home screen

---

## One-time setup

### Smart Import (Claude API key)

Smart Import uses Claude to read booking emails and extract all the details automatically.

1. Go to [console.anthropic.com](https://console.anthropic.com) and sign up
2. Go to **API Keys → Create Key** and copy it
3. In the app: **Settings → Smart Import** → paste your key and tap Save

Costs a fraction of a penny per import.

### Google Sheets Sync

Syncs your data between phone and computer automatically. Free via Google Cloud.

1. Go to [console.cloud.google.com](https://console.cloud.google.com)
2. Create a new project — name it "Holiday App"
3. Go to **APIs & Services → Library** and enable:
   - **Google Sheets API**
   - **Google Drive API**
4. Go to **Credentials → Create Credentials → OAuth 2.0 Client ID**
   - Application type: **Web application**
   - Add your GitHub Pages URL to **Authorised JavaScript origins** (e.g. `https://yourusername.github.io`)
5. Copy the **Client ID**
6. In the app: **Settings → Google Sheets Sync** → paste the Client ID → Save → Sign in with Google

The app will create a "Holiday Companion" spreadsheet in your Google Drive automatically. To use on a second device, open the app, repeat steps 5–6 with the same Google account, then tap Sync now.

---

## How to use

1. Go to **Settings** and add your family under **Your Travellers** — passport details stored once, used on every trip
2. Tap **＋ New holiday** to create a trip and select who's coming
3. Use **✨ Smart Import** to paste booking confirmation emails — Claude fills in all the details for you to review and confirm
4. Or tap **＋ Add item** to add flights, stays, activities and notes manually
5. Add payments in the **Money** tab as you pay them — track deposits, balances due, and on-arrival payments
6. Add emergency contacts in the **Emergency** tab before you travel — one tap to call, works offline
7. Upload booking PDFs and documents in **Documents** while on WiFi — available offline when you need them

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire app |
| `sw.js` | Service worker — enables offline access |
| `manifest.json` | Makes it installable as a home screen app |
| `README.md` | This guide |

---

## Data & privacy

- All data is stored locally on your device (browser localStorage)
- Google Sheets sync stores data in **your own Google Drive** — nobody else has access
- Documents are stored on-device only and are not synced to Sheets
- API keys are stored locally and sent only to their respective APIs (Anthropic, Google)
- Nothing is sent to any third-party server
- The GitHub repository is public (the code is visible) but contains no personal data

**Recommended:** enable two-factor authentication on your Google account and keep your phone screen locked.
