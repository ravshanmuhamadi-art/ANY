noor_app
Noor - Islamic Companion App
Getting Started
This project is a starting point for a Flutter application.
A few resources to get you started if this is your first Flutter project:
•
Learn Flutter
•
Write your first Flutter app
•
Flutter learning resources
For help getting started with Flutter development, view the online documentation, which offers tutorials, samples, guidance on mobile development, and a full API reference.
Sajda-Backed Prayer Times
Al Taqweem uses authorized Sajda public prayer-times pages as the primary prayer-time source when no manual Advanced calculation override is active. The backend discovers Sajda city pages, parses monthly tables, saves daily documents to Firestore, and lets the app read/cache the result without repeatedly touching Sajda.
Priority order:
1.
Manual Advanced calculation settings (method, madhab, high-latitude rule)
2.
Sajda Times local cache
3.
Sajda Firestore daily document
4.
Firebase Function on-demand monthly fetch from Sajda
5.
Existing profile / official-source / Aladhan / local adhan fallback
Manual per-prayer tune offsets are applied on top of Sajda times, so the user can still adjust individual prayers without disabling the Sajda source.
Sajda location discovery documents are stored at:
sajda_locations_v1/{sajdaCityId}
Example Dubai location:
{
  "sajdaCityId": "292223",
  "countrySlug": "united-arab-emirates",
  "citySlug": "dubai",
  "cityName": "Dubai",
  "countryName": "United Arab Emirates",
  "cityNameKey": "dubai",
  "countryNameKey": "united-arab-emirates",
  "timezone": "Asia/Dubai",
  "latitude": 25.2048,}