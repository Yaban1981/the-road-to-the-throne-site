# The Road to The Throne — Québec HC

Static interest form (FR/EN) to build lineups for Boston Showdown, Montreal Meltdown, and The Throne.

## Structure
```
the-road-to-the-throne-site/
├─ index.html
└─ logos/
   ├─ qhc.png
   ├─ throne.png
   ├─ bluechip.png
   └─ meltdown.png
```

> Put your **PNG logos** in `/logos` with the exact filenames above.

## Deploy (GitHub → Vercel)

### 1) Create repo & push (PowerShell)
```powershell
cd C:\TMP
mkdir the-road-to-the-throne-site -ea 0
cd the-road-to-the-throne-site

# Copy the downloaded files into this folder (index.html + /logos)

git init
git add .
git commit -m "Initial commit: The Road to The Throne form"
git branch -M main
git remote add origin https://github.com/<TON_USER>/the-road-to-the-throne-site.git
git push -u origin main
```

### 2) Vercel (web UI — easiest)
- Go to **vercel.com** → **New Project** → **Import Git Repository**.
- Select `the-road-to-the-throne-site`.
- **Framework Preset:** *Other* (static).
- **Build & Output Settings:** Leave defaults (output = `/`).
- Click **Deploy** → you’ll get a public URL.

> CLI alternative:
```powershell
npm i -g vercel
vercel login
vercel deploy --prod
```

## Email routing
The form uses **FormSubmit** to email submissions to `yannick.banaszak@outlook.com` with a hidden BCC to Dave.
On first use, FormSubmit may send a **verification email** once.
