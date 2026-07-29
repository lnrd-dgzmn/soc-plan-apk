# Build your SOC Plan APK (free, no tools to install)

This project builds a **real, installable Android APK** in the cloud using GitHub Actions.
You don't install Android Studio or any SDK — GitHub's servers do the compiling for free.
At the end you download an `app-debug.apk` straight to your phone and install it.

Everything you need is already in this folder. Just follow the steps.

---

## What you need
- A free GitHub account (github.com). Bonus: this becomes your first public repo — the kind
  employers ask to see when you apply for SOC roles.

---

## Step 1 — Create a repository
1. On github.com, click **+ → New repository**.
2. Name it `soc-plan-apk`, keep it **Public**, click **Create repository**.

## Step 2 — Upload these files
1. On the new empty repo page, click **uploading an existing file**.
2. Unzip this project on your computer, then **drag the CONTENTS of the folder** into the upload box
   — meaning `settings.gradle`, `build.gradle`, the `app` folder, and the `.github` folder should
   land at the **top level** of the repo (not inside another folder).
3. Scroll down, click **Commit changes**.

> Tip: if you don't see the `.github` folder when dragging, it's hidden. On Windows enable
> "Hidden items" in File Explorer's View menu; on Mac press Cmd+Shift+period to show hidden files.

## Step 3 — Let it build
Uploading to the `main` branch automatically starts the build.
1. Click the **Actions** tab. You'll see a run called **Build APK** with a spinning icon.
2. Wait about 3–5 minutes for it to turn into a green check.
   (If it ever fails, open the failed step, copy the red error text, and send it to me — I'll fix it.)

## Step 4 — Download the APK to your phone
Once the run is green, open your repo **on your phone's browser** and either:
- **Easiest:** tap **Releases** (right side of the repo home page) → **SOC Plan APK** →
  download **`app-debug.apk`** directly. No unzipping.
- Or: **Actions** tab → the green run → **Artifacts** → **SOC-Plan-APK** (this one downloads as a .zip
  you'll need to unzip first).

## Step 5 — Install it
1. Tap the downloaded `app-debug.apk`.
2. Android will ask to allow installing from your browser/Files app — allow it.
3. You may see "unknown developer" — that's normal for an app you built yourself. Tap **Install**.
4. Open **SOC Plan** from your app drawer. Your ticked progress saves right on the phone.

---

## Good to know (honest notes)
- This is a **debug-signed** APK — perfect for installing on your own phone and sharing.
  For the Google Play Store you'd need a **release** build with your own signing key; ping me when
  you're ready and I'll add that.
- The app works fully offline. The only online part is loading nice fonts the first time; offline it
  falls back to system fonts and still works.
- Want changes before you build (e.g. a countdown to your exam date, or study-time logging)?
  Tell me and I'll update the files first.

---

## Prefer not to use GitHub?
There are online "HTML to APK" converters and pwabuilder.com that can also produce an APK, but they're
usually ad-supported and you have less control over privacy. The GitHub route above is free, clean,
and gives you a repo you can actually show off. Your call.
