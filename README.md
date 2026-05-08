# 🎯 Training Tracker — A Girl & A Gun Women's Shooting League

A mobile-friendly training log built for shooters. Track your dry fire, live fire, fitness, and other training activities day by day — add weekly reflections and monthly victories — all from your iPhone, iPad, or laptop browser. No app store required.

---

## What It Does

- **Daily activity logging** — tap any day to check off Dry Fire, Live Fire, Fitness, or Other (with a custom note field)
- **Weekly summaries** — reflect on your big wins, ah-ha moments, and changes to make
- **Monthly victories** — capture what you achieved, insights you gained, and what you're looking forward to
- **Month navigation** — browse forward and back through any month
- **Print / Save as PDF** — print a clean copy of any month for your records
- **Works like an app** — add it to your iPhone or iPad home screen from Safari and it opens fullscreen with no browser bar
- **Cloud sync** — data saves to your own private Google Sheet, so it's available on every device and survives any code updates

---

## Want Your Own Copy? You're Welcome To It! 🙌

Feel free to fork this repository and make it your own. Whether you're part of AG&G or just a shooter who loves tracking progress, the more people using it the better!

Here's what you'll need to do to get your own fully working version up and running. It takes about 15–20 minutes total and you don't need any coding experience.

---

## Setup Instructions

### Step 1 — Fork This Repository

1. Click the **Fork** button at the top right of this page
2. GitHub will create a copy of this repository under your own account
3. Go to **Settings → Pages** in your new repository
4. Under Source, select **Deploy from a branch** → choose `main` → click **Save**
5. After about 60 seconds your app will be live at:
   `https://yourusername.github.io/training-tracker`

---

### Step 2 — Create Your Own Google Sheet

> ⚠️ **This step is important.** Each person needs their own Google Sheet. Please don't skip this — if you use someone else's sheet URL, your data will mix with theirs!

1. Go to [sheets.google.com](https://sheets.google.com)
2. Click **+** to create a new blank spreadsheet
3. Name it something like **My Training Tracker Data**

---

### Step 3 — Set Up the Apps Script

1. In your Google Sheet, click **Extensions → Apps Script**
2. A new tab opens — delete all the placeholder code in the editor
3. Copy the entire contents of the **`Code.gs`** file from this repository
4. Paste it into the Apps Script editor
5. Click the **💾 Save** icon and name the project **Training Tracker**

---

### Step 4 — Deploy as a Web App

1. Click **Deploy → New deployment**
2. Click the **gear icon ⚙** next to "Select type" → choose **Web app**
3. Set the following:
   - **Execute as:** Me
   - **Who has access:** Anyone
4. Click **Deploy**
5. Google will ask you to authorize — click through the permissions screens
   - If you see an "unsafe" warning, click **Advanced → Go to Training Tracker → Allow**
   - This warning is normal for personal scripts and just means Google hasn't formally reviewed it
6. Copy the **Web App URL** that appears — it looks like:
   `https://script.google.com/macros/s/LONG_CODE_HERE/exec`

---

### Step 5 — Connect Your Sheet to the App

1. Download **`index.html`** from your forked repository
2. Open it in a text editor (TextEdit on Mac, Notepad on Windows)
3. Find this line near the top of the JavaScript section:
   ```
   const SCRIPT_URL = "YOUR_APPS_SCRIPT_URL_HERE";
   ```
4. Replace `YOUR_APPS_SCRIPT_URL_HERE` with the URL you copied in Step 4:
   ```
   const SCRIPT_URL = "https://script.google.com/macros/s/LONG_CODE_HERE/exec";
   ```
5. Save the file

---

### Step 6 — Upload to GitHub

1. Go to your forked repository on GitHub
2. Click **Add file → Upload files**
3. Drag in your updated `index.html`
4. Click **Commit changes**
5. Wait about 60 seconds for GitHub Pages to rebuild

---

### Step 7 — Add to Your iPhone Home Screen

1. Open your GitHub Pages URL in **Safari** on your iPhone
2. Tap the **Share** button (the box with an arrow at the bottom)
3. Scroll down and tap **Add to Home Screen**
4. Name it **Training Tracker** and tap **Add**

It will now appear on your home screen and open like a full-screen app! 🎉

---

## Using It on Multiple Devices

Once set up, your data automatically syncs across all your devices — iPhone, iPad, laptop — because everything saves to your personal Google Sheet. Log a session on your phone in the morning and it'll be there when you open it on your iPad that evening.

You can also open your Google Sheet at any time to view all your raw data, export it, or make manual corrections if needed.

---

## Troubleshooting

**"Offline — changes won't save" appears**
- Double-check the `SCRIPT_URL` in `index.html` — make sure there are no extra spaces or missing characters
- Make sure you deployed the Apps Script with **Who has access: Anyone**
- Try redeploying: Apps Script → Deploy → Manage deployments → Edit (pencil icon) → New version → Deploy

**Data isn't showing on a second device**
- Make sure both devices are connected to the internet
- On iPhone: close and reopen the app
- On laptop: hold Shift and click Reload for a hard refresh

**The icon isn't updating on my iPhone home screen**
- iOS caches the icon aggressively
- Delete the shortcut from your home screen and re-add it from Safari

---

## Updating the App in the Future

Your Google Sheet data is completely separate from the app code, so you can update `index.html` on GitHub anytime without losing a single entry. Just upload the new file and your data stays right where it is.

---

## Built With

- Vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies
- Google Apps Script as a lightweight backend
- Google Sheets as a free personal database
- GitHub Pages for free hosting

---

*Made with 💜 for the AG&G Women's Shooting League community*
