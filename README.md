Naya Nepal — mobile app MVP
A React Native / Expo starter for a citizen-led Nepal initiative focused on:
social responsibility and volunteering
legal awareness using official sources
environmental conservation
civic issue reporting and status tracking
Included
Expo mobile app with Home, Report, Learn, Actions, and Profile tabs
Demo mode that works without a backend (sample content only; reports remain local to the running app)
Optional Supabase integration for submitting and listing community reports
Database schema with Row Level Security (RLS)
English/Nepali-ready UI labels (initial UI is English)
Important limitations
This is an MVP starter, not a finished national public-service system. Before public launch, add authentication, moderation workflows, abuse reporting, accessibility testing, Nepali translation review, privacy/legal review, backup/monitoring, and a signed-off municipal referral process. Do not use it for emergencies. It is not an official Government of Nepal app and has no government endorsement.
Run it
Install Node.js LTS and Git.
Unzip this folder.
In this folder, run:
npm install
Optional backend:
Create a project at https://supabase.com
Open SQL Editor and run supabase/schema.sql
Copy .env.example to .env
Set EXPO_PUBLIC_SUPABASE_URL and EXPO_PUBLIC_SUPABASE_ANON_KEY
Never put a Supabase service-role key in a mobile app.
Start:
npx expo start
Install Expo Go on your Android phone and scan the QR code, or press a if Android tooling is installed.
Supabase notes
The database schema enables RLS. Reports can be created anonymously with restricted fields; the public read policy only exposes non-sensitive reports. Before real deployment, prefer authenticated submissions, rate limiting, CAPTCHA/anti-spam, storage policies for images, and a verified staff-only status update workflow. The demo uses only text reports and does not upload images.
Suggested production roadmap
Phase 1: pilot in one municipality; confirm partner and report categories
Phase 2: authentication, admin review queue, official referrals, audit logs
Phase 3: Nepali translation, low-data mode, accessibility, privacy impact assessment
Phase 4: independent evaluation before expanding to other municipalities