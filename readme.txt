Install as an app (Windows 11)
==============================

Use Microsoft Edge (recommended for Windows PWAs):

Open the site in Edge.

Click … (menu) → Apps → Install this site as an app.

Launch it from the Start menu.

Make it start automatically on Windows 11
=========================================

After installing:

Option A — Windows “Startup apps”

Settings → Apps → Startup

Find your installed PWA (it often appears as the app name you installed).

Toggle it On.

Option B — Task Scheduler (reliable)

Create a task “At log on” that runs:

msedge.exe --app="http://localhost:8080/"

(Replace the URL with where you host it.)

About “automatically start” audio
=================================

Even if the app opens at login, audio will usually stay blocked until you click Start once (that’s a browser security rule). If you need true unattended audio (no click), the practical approaches are:

A kiosk / managed device configuration (Edge policies / assigned access) where autoplay restrictions can be handled via enterprise controls.

A native app (not a web app) for unrestricted startup audio.