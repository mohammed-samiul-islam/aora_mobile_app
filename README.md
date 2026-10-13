# Aora

A React Native (Expo) mobile app for sharing short videos, backed by Appwrite for auth, database and file storage.

## Features

- Sign up / sign in / sign out (Appwrite accounts)
- Home feed with all posts and a "Trending" carousel of latest posts
- Search videos (`/search/[query]`)
- Create screen: pick a video and thumbnail (expo-image-picker) and upload to Appwrite storage
- Profile screen showing the user's own posts
- Bookmark tab
- File-based routing with Expo Router; styling with NativeWind

## Tech Stack

React Native · Expo (Router, AV, Image Picker) · NativeWind (Tailwind) · Appwrite (`react-native-appwrite`) · React Native Animatable

## Project Structure

```
app/
  (auth)/        # sign-in, sign-up
  (tabs)/        # home, create, bookmark, profile
  search/[query].jsx
components/      # VideoCard, Trending, SearchInput, FormField, CustomButton, EmptyState, InfoBox
context/GlobalProvider.js
lib/appwrite.js  # Appwrite config + API helpers
lib/useAppwrite.js
```

## Getting Started

```bash
npm install
npx expo start        # or: npm start
npm run android       # / npm run ios / npm run web
```

Other scripts: `npm test` (Jest), `npm run lint`.

Appwrite settings (endpoint, project ID, database/collection/storage IDs) are configured directly in `lib/appwrite.js`; update them to point at your own Appwrite project.
