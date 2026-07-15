# Admission Register — PWA

## GitHub par upload karne ke steps

1. GitHub par ek naya repo banao (ya existing wala use karo)
2. Is folder ki saari files (`index.html`, `manifest.json`, `sw.js`, `icons/` folder) repo ke **root** mein upload karo — same folder structure rakhna zaroori hai
3. Repo → **Settings → Pages** mein jao
4. Source: **Deploy from a branch**, Branch: `main`, folder: `/root` select karo, **Save**
5. Kuch minute baad ek URL milega jaisa: `https://<username>.github.io/<repo-name>/`
6. Us URL ko browser mein khol ke test kar lo — password screen aani chahiye, login karke register khulna chahiye

## PWABuilder se Android app banane ke steps

1. https://www.pwabuilder.com par jao
2. Apna GitHub Pages URL paste karo (e.g. `https://<username>.github.io/<repo-name>/`)
3. "Start" dabao — PWABuilder manifest aur service worker detect kar lega
4. **Android** package option select karo
5. Package generate hone do, `.aab`/`.apk` download kar lo
6. Us file ko phone mein install karke test karo

## Files kya hain

- `index.html` — poora app (UI + logic + Supabase connection)
- `manifest.json` — PWA metadata (naam, icon, colors)
- `sw.js` — service worker, offline mein app-shell cache karta hai
- `icons/` — app icons (192x192, 512x512, aur maskable version)

## Zaroori baat

- Data Supabase cloud mein store hota hai — internet chahiye add/edit/delete ke liye
- Password login hai (client-side) — casual protection ke liye theek hai, high-security ke liye nahi
- Agar HTML/CSS/JS mein koi badlav karna ho, sirf `index.html` edit karna hai
