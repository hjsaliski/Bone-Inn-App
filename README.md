# Bone Inn app

Starter scaffold. Covers sign up, dog profile creation, discover/swipe with
tap-to-expand detail, matches list, chat, and report/block.

## Setup

1. Install Node.js (LTS) if you don't have it: https://nodejs.org
2. Install the Expo Go app on your iPhone from the App Store.
3. From this folder, run:
   ```
   npm install
   ```
4. Copy `.env.example` to `.env` and fill in your actual Supabase project URL
   and anon key. Find these in your Supabase project under
   Project Settings > API.
5. Run:
   ```
   npx expo start
   ```
6. Scan the QR code shown in the terminal with your iPhone's camera. It will
   open the app inside Expo Go.

## What's not built yet

- Photo upload to Supabase Storage (currently only reads photo_urls if
  present, doesn't let you add one yet)
- Location-based distance filtering (schema has zip_code/neighborhood but
  discover screen doesn't filter by it yet)
- Match celebration screen (currently a match just gets written to the
  database silently, no popup shown)
- Push notifications for new matches/messages
- Account deletion flow, required by Apple before App Store submission
- Liability waiver acceptance at sign up

## Before submitting to the App Store

- Apple Developer account, $99/year
- Privacy policy and terms of service, especially a liability waiver given
  this app arranges in-person meetups
- Account deletion flow
- EAS Build for the actual iOS binary: `npx eas build --platform ios`
  (requires an Expo account, free to create)
