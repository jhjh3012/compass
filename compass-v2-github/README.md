# Compass — personal school app prototype

A mobile-first, standalone recreation of the screens demonstrated in the supplied recordings. Uses plain HTML, CSS and JavaScript. No build or installation required.

## Put it on GitHub

1. Create or open a GitHub repository.
2. Upload `index.html`, `style.css`, and `script.js` together at the repository root.
3. In the repository's **Settings → Pages**, select **Deploy from a branch**, choose your main branch and **/ (root)**, then save.
4. Open the published GitHub Pages address once deployment finishes.
5. On iPhone, open that address in Safari and choose **Share → Add to Home Screen** for an app-like view.

You can also open `index.html` locally for a quick preview. Hosting is recommended for consistent browser storage. No server or API keys are needed.

## Hidden profile editor

Open **More → the profile row → Dashboard**. Tap the circular profile photo **three times within 1.4 seconds**. The editor lets you change the photo from the device photo picker, name, gender, age, date of birth, year level, student ID, group, house, school, and email.

Choose **Save changes** to keep edits. Cancel or Escape discards unsaved edits. Photos are resized locally before storage; nothing is uploaded. Age and date of birth are separately editable. Data stays in this browser on this device and does not sync; clearing site data removes it. The hidden gesture is a shortcut, not password protection.

## Included

- Home timetable, expandable news, and navigation.
- Calendar day/week/month views and date navigation.
- Notifications and mark-all-read.
- More screen with the demonstrated tile layout.
- Profile Dashboard, sample Chronicle and Attendance, Reports empty state.
- Triple-tap profile editor, device photo picker, persistent profile data.
- Responsive phone layout and iPhone safe-area support.

## Scope

This is a personal prototype, not the official Compass application. It uses sample student details and records. It does not connect to school systems, submit absences, verify identity, make purchases, retrieve reports, or reproduce unavailable attachments. Tiles needing those services open explanatory panels. The recordings do not show those underlying workflows. No login credentials are collected.

## Updating an existing deployment — version 2

Replace all three app files in the same GitHub folder as the existing version. Commit the changes and let your connected Cloudflare deployment finish. Keep the same site address to retain saved profile details. Reload the app after deployment; the versioned stylesheet and script links help avoid old cached files.

This update refines the iPhone typography, timetable rows, curved Favourites section, news cards, Compass mark, navigation and More tiles, including the lower settings controls. It adds no school logo.

Home, Calendar and the profile share the selected date and timetable. All class-code year prefixes use your saved year level, including event detail dialogs. Personal IDs and manually entered group names are left as entered. Wednesday uses the timetable from the supplied screenshot; other weekdays use the original sample schedule. Weekends have no lessons. These remain sample timetables, not actual school scheduling or holiday data.

The app opens on the device's current local date and checks for day changes while open or when returning to the app. News dates roll relative to today; these are sample announcements, not live school news. Saved profile fields and photos continue to use the existing storage key.

Verified with interaction checks: timetable consistency, year changes, detail dialogs, weekends, midnight and year rollover, relative news dates, and the More screen sections. Exact visual matching and camera-roll selection still require verification on the deployed app / iPhone.
