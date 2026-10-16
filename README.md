# SHREE BILESHWER COMPUTERS — Android App

Gujarati-first dashboard with a banner carousel for published courses and ads, daily updates, six main categories, and a menu for About, Results, Resume, Age Calculator, Biodata, Current Recruitment, Photo Resize, Graduate Jobs, and Online Form Center.

## Build a test APK
1. Open the **Actions** tab.
2. Select **Build Android APK** and tap **Run workflow**.
3. After the workflow succeeds, open the run and download the `shree-bileshwer-computers-debug-apk` artifact ZIP.
4. Extract the ZIP to find `app-debug.apk`.

This is a debug/test APK, not a Play Store-signed release.

## Admin content
The app reads published records from the existing Supabase `public.content_items` table. Banner items use `ads` and `courses`; other category IDs are defined in `app/src/main/assets/index.html`. The public app only uses a publishable Supabase key; never put a service-role or secret key in a client app.
