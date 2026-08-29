# MedBrain AI – Professional Healthcare App

**Your AI Co-Pilot in Better Healthcare**

Complete mobile-first web application for Doctors & Patients with AI support, digital prescriptions, real-time monitoring, and patient data management (up to 100 patients).

---

## Features

### Doctor Side
- AI Voice Scribe (real microphone + speech-to-text)
- Differential Diagnosis
- Digital Prescription + QR Code
- Real-time Vitals Monitoring
- Secure Patient Chat
- Full Patient Journey (Appointment → Discharge)

### Patient Side
- Appointment Booking + Video Call
- Medicine Reminders
- Symptom Diary
- Lab Reports with AI Explanation
- Health Records Vault
- Family Profiles
- Emergency SOS
- Multilingual (EN / हिन्दी)

### Data System
- Up to **100 patients** storage
- Local backup (JSON export/import)
- Auto-save in browser

---

## Project Structure

```
medbrain-ai/
├── index.html              # Main application
├── manifest.json           # PWA configuration
├── sw.js                   # Service Worker (offline support)
├── js/
│   └── data-manager.js     # Patient database + backup system
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── README.md
```

---

## How to Publish (Professional Setup)

### Step 1: Create GitHub Repository

1. Go to [github.com](https://github.com) → Sign up / Login
2. Click **New repository**
3. Name: `medbrain-ai`
4. Keep it **Public**
5. Click **Create repository**

### Step 2: Upload Code to GitHub

**Method A – Drag & Drop (Easiest)**
1. Open your new repository
2. Click **uploading an existing file**
3. Drag the entire `medbrain-ai` folder contents
4. Click **Commit changes**

**Method B – Using Git (Advanced)**
```bash
git init
git add .
git commit -m "Initial commit - MedBrain AI"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/medbrain-ai.git
git push -u origin main
```

### Step 3: Connect to Netlify (Auto Deploy)

1. Go to [netlify.com](https://netlify.com) → Sign up with **GitHub**
2. Click **Add new site** → **Import an existing project**
3. Choose your `medbrain-ai` repository
4. Settings:
   - Build command: leave empty
   - Publish directory: `/` (root)
5. Click **Deploy site**

**Done!**  
Ab se jab bhi aap GitHub pe code update karoge → Netlify automatically naya version live kar dega.

---

## How to Update the App Later

1. Apne computer pe `index.html` ya koi file change karo
2. GitHub pe jaake updated file upload / push karo
3. Netlify 30–60 seconds me auto-update kar dega

Koi manual drag-drop nahi karna padega.

---

## Patient Data Backup System (100 Patients)

App me built-in data manager hai:

### Features
- Maximum **100 patients** store ho sakte hain
- Data browser ke localStorage me save hota hai
- **Export Backup** → JSON file download
- **Import Backup** → pehle se save kiya hua data restore

### How to Backup
1. Doctor login karo
2. Browser me right-click → Inspect → Console
3. Type: `MedBrainDB.exportBackup()`
4. JSON file download ho jayegi

### How to Restore
1. Backup JSON file ready rakho
2. Console me:
```js
// File input se import (or use UI later)
```

### Console Commands
```js
MedBrainDB.getAll()           // Saare patients dekho
MedBrainDB.stats()            // Kitne patients hain
MedBrainDB.exportBackup()     // Backup download
MedBrainDB.clearAll()         // Saara data delete
```

---

## Custom Domain (Optional)

1. Netlify dashboard → Domain settings
2. Add custom domain (example: `app.medbrain.ai`)
3. Domain provider pe DNS records add karo
4. Free HTTPS automatically mil jayega

---

## Future Upgrades (Recommended Order)

1. **Supabase / Firebase** → Real database + authentication
2. **Real AI** → Grok / OpenAI API connect
3. **Push Notifications** → Medicine reminders
4. **Play Store** → Capacitor se Android app
5. **Multi-clinic support**

---

## Local Development

```bash
npx serve .
# or
python -m http.server 3000
```

Then open `http://localhost:3000`

---

## Support

App fully client-side hai.  
Data user ke browser me store hota hai.  
Regular backup zaroor lete rehna.

---

**MedBrain AI** – Built for Indian doctors & patients.
