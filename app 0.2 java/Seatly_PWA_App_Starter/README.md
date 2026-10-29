# Seatly PWA Starter (free installable web app)

This package wraps the **standalone Seatly preview** as a Progressive Web App (PWA), so it can be installed from a browser like an app. You do not need Android Studio just to install it on a phone.

## Publish it free using GitHub Pages

1. Sign in to GitHub and create a **public** repository named `seatly-app`.
2. Upload every file and folder from this package to the repository root. The root should contain `index.html`, `manifest.webmanifest`, `sw.js`, and `icons/`.
3. Open **Settings → Pages**.
4. Under Build and deployment, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
5. Wait until GitHub Pages shows the published HTTPS URL. Open that URL on your phone.
6. On Android Chrome, tap **⋮ → Install app** or **Add to Home screen**. On desktop Edge, use the install icon in the address bar or **Apps → Install this site as an app**.

## Important limitations

- A PWA must be served from HTTPS (GitHub Pages provides HTTPS). Opening `index.html` from `C:\Downloads` is not enough to install it.
- This is the offline **demo preview**. Accounts, students, and seating changes are stored in that browser/device. They do **not** sync across students' phones.
- If every student must use an account and see faculty updates across devices, deploy the Java Spring Boot backend and use a shared persistent database. GitHub Pages hosts only static frontend files; it cannot run the Java backend.
- The service worker caches the app shell for repeat/offline opening, but login/data operations should not be expected to sync or work cross-device while offline.

## Demo accounts

- Faculty: `faculty` / `Faculty@123`
- Student: `99250040078` / `Student@123`

For a class demonstration, use the demo role buttons on the sign-in screen. Do not reuse these demo passwords for real accounts.
