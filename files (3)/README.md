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

## Version 3

Replace index.html, style.css and script.js together. This version uses Compass’s published vector wordmark (embedded in the script) and bundled Roboto fonts (embedded in the stylesheet), so there are no extra image/font folders to upload. Retain FONT-LICENSE.txt with the project.

Logo source: https://www.compass.education/wp-content/uploads/2024/02/Compass-Logo-Main-on-light-bg-rgb.svg
Font source: Google Fonts, Roboto; see FONT-LICENSE.txt.

Adjusted timetable card colours, calendar spacing, notification typography, and the profile’s smaller text. The website always starts on the device’s current local day. Safari back/forward-cache restoration also resets the selected day to today. Normal in-app navigation preserves your selected day across Home, Calendar and Dashboard. Class details in the week view use the day of the selected event.

Checks cover year changes, Home/Calendar/Profile consistency, week event details, day/year rollover and Safari page restoration. Visual pixel equality with the native app has not been verified; browser font rendering and device safe areas can differ.

## Version 4 — profile screen refinement

Replace all three app files together: index.html, style.css and script.js. Keep FONT-LICENSE.txt in the project. The new version links bypass the previous stylesheet/script cache. Existing saved profile details and photos are preserved at the same site address.

The subject is now **Mathematics**, with no Beta suffix. Home, Calendar and Dashboard all read the same ordered timetable entries and cancellation statuses. The Friday sample includes the green work-experience entry and cancelled lessons from the supplied reference. Other weekdays retain the sample lesson schedule; weekends remain empty. These are illustrative schedules, not live school records.

The profile layout now follows the supplied screenshot's dimensions more closely: a 90-point photo, larger name and details, segmented tabs with separators, 30-point attendance squares, a larger date strip, and 60-point lesson cards. The profile date picker also has a Go to today option under its three-dot button.

Verified: all seven Friday entries and their statuses match across the three views; Mathematics is consistent; year prefixes, week event details, current local date, midnight/year rollover and Safari restored-page dates pass interaction checks. Pixel-for-pixel appearance on a physical iPhone remains unverified.

## Version 5 — home screen icon and smoother navigation

Replace all four files together: index.html, style.css, script.js, and the new apple-touch-icon.png (upload it to the same repository root as the others). Keep FONT-LICENSE.txt in the project. The new version links bypass the previous stylesheet/script cache. Existing saved profile details and photos are preserved at the same site address, and the sample timetable is unchanged from version 4.

Adding the site to the iPhone home screen now shows a proper app icon (a filled version of the existing compass mark) instead of a page screenshot — this requires the `apple-touch-icon.png` file to actually be uploaded next to `index.html`; without it, iOS falls back to a screenshot again. If you already added the site to your home screen before this update, remove that shortcut and re-add it, since iOS caches the icon it captured the first time.

Page and tab switches now use the browser's View Transition API for a smooth crossfade on iOS 18+/Safari 18+, with a plain fade fallback on older Safari versions, and respect the "Reduce Motion" accessibility setting. Buttons, tiles, tabs and notifications also get a brief press animation (dim/scale) for more immediate tap feedback.

## Version 6 — timetable matched to a Compass School Manager screenshot

Replace all four app files together (index.html, style.css, script.js, apple-touch-icon.png); keep FONT-LICENSE.txt. Existing saved profile details and photos are preserved at the same site address.

The header logo already matched the official Compass lockup (icon + wordmark) pixel-for-pixel before this update, using the same source asset supplied earlier — no change was needed there.

The default weekday timetable (used for any day other than the Wednesday and Friday samples) was replaced to match a supplied Tuesday 13 October screenshot exactly: 10HRC4 Homeroom E4 DCOD, 10MATB1 Mathematics A5 COOD, 10HSIE4 Human Society and Its Environment E4 DCOD, 10ENG5 English E5 PROA (11:15am and 12:15pm), and 10PDE4 Personal Development, Health and Physical Education DEM4 BRAD — with "Mathematics" (no "Beta" suffix), same as before. Start times match the screenshot; end times follow the existing period grid, since the screenshot only shows start times. The Home screen's bullet separators now match the screenshot's "•" character. Wednesday and Friday keep their previously supplied sample schedules.

Weekends already showed no lessons. School holidays now do too, once you fill them in: near the top of script.js is a `holidayRanges` array, empty by default. Add date ranges like `['2026-12-19','2027-01-27']` (inclusive, YYYY-MM-DD) for your school's actual term breaks and those dates will show no classes as well. I don't have your school's real term dates, so this needed to be left for you to fill in rather than guessed.

## Version 7 — new app icon and unified timetable

Replace all four app files together (index.html, script.js, style.css, apple-touch-icon.png); keep FONT-LICENSE.txt. Saved profile details and photos are preserved at the same site address.

The home screen icon (`apple-touch-icon.png`) is now the stopwatch-style Compass logo on a white background. If you already added the site to your home screen, remove that shortcut and re-add it so iOS picks up the new icon.

Every weekday now uses the timetable from the supplied Wednesday 14 October screenshot: 10HRC4 Homeroom, 10MATB1 Mathematics (twice), 10COM3 Commerce (twice) and 10SCI4 Science, with the subject shown as "Mathematics" (no "Beta"). Home, Calendar (day, week) and the profile all read the same list. Weekends and any `holidayRanges` still show no classes. The Friday work-experience entry is unchanged.
