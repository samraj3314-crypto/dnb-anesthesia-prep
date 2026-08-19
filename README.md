# DNB Anaesthesia Prep — GitHub Pages PWA

A no-APK, installable web app for DNB Anaesthesia question practice.

## Included
- Section-wise question bank
- Daily random question (changes by calendar day)
- Competitive-exam style MCQs with shuffled order
- Countdown timer
- Score and explanations
- Local progress/streak tracking
- Daily study reminder setting
- Browser notifications where supported
- Offline cache / PWA install support
- GitHub Pages deployment via GitHub Actions

## Deploy on GitHub
1. Create a new GitHub repository, e.g. `dnb-anesthesia-prep`.
2. Upload all files from this folder, preserving `.github/workflows/deploy.yml`.
3. Commit to the `main` branch.
4. Go to **Settings → Pages → Build and deployment → Source → GitHub Actions**.
5. Open the **Actions** tab and wait for **Deploy DNB Anaesthesia Prep to GitHub Pages** to finish.
6. The site will be available at `https://YOUR-USERNAME.github.io/dnb-anesthesia-prep/`.

## Add questions
Edit `app.js` and add objects to the `questions` array:

`{id:25,s:'pharmacology',q:'Question?',o:['A','B','C','D'],a:1,e:'Explanation'}`

The `a` value is zero-based: 0=A, 1=B, 2=C, 3=D.

## Notification limitation
The app can request browser notification permission and can remind the user while the PWA/browser is running or has a background execution opportunity. GitHub Pages alone does not provide a reliable server-side scheduler that can wake a fully closed browser at an exact future time. For guaranteed push notifications, add a Web Push backend (VAPID + subscription storage) later.
