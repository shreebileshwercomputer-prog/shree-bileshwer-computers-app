# SHREE BILESHWER COMPUTERS — Android App

Gujarati-first dashboard with a banner carousel for published courses and ads, daily updates, six main categories, and a menu for About, Results, Resume, Age Calculator, Biodata, Current Recruitment, Photo Resize, Graduate Jobs, and Online Form Center.

## Build a test APK with Codemagic
1. Open the project in Codemagic and connect/select this GitHub repository.
2. Ensure Codemagic is configured to use the repository's `codemagic.yaml` file and the `android-apk` workflow.
3. Start a build for the `main` branch (pushes to `main` are configured to trigger builds automatically).
4. After the build succeeds, download `app-debug.apk` from the build's Artifacts section.

This is a debug/test APK, not a Play Store-signed release. GitHub Actions also has a separate workflow file, but the intended APK build process is Codemagic.

## Admin content
The app reads published records from the existing Supabase `public.content_items` table. Banner items use `ads` and `courses`; other category IDs are defined in `app/src/main/assets/index.html`. The public app only uses a publishable Supabase key; never put a service-role or secret key in a client app.
