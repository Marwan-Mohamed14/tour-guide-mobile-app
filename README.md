# Tour Guide — Smart Tourism Discovery App

![Flutter](https://img.shields.io/badge/Flutter-3.8+-02569B?style=flat&logo=flutter&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-Firestore%20%7C%20Auth-FFCA28?style=flat&logo=firebase&logoColor=black)
![Dart](https://img.shields.io/badge/Dart-3.0+-0175C2?style=flat&logo=dart&logoColor=white)
![Geoapify](https://img.shields.io/badge/Geoapify-Places_API-4285F4?style=flat)

A cross-platform tourism discovery mobile application that helps users explore points of interest near their location. The app uses the **Geoapify Places API** to search across 13 categories (museums, restaurants, parks, mosques, cafes, cinemas, and more), lets users save favorites and schedule future visits with reminder notifications, and supports both **Arabic and English** languages. It includes full offline support using cached data so users can browse saved places without an internet connection.

---

## Features

- **Location-Based Discovery** — Automatically detects your GPS location and surfaces nearby places across 13 categories using parallel Geoapify API calls
- **Place Details** — View place name, address, distance, coordinates, and Wikipedia links for each location
- **Favorites** — Save and manage favorite places synced to Firebase Firestore
- **Visit Scheduler** — Add places to a personal visit list with a scheduled date and receive notification reminders
- **Bilingual Support** — Full Arabic and English interface with persisted language preference
- **Offline Mode** — Browse cached places when there is no internet connection; automatic redirect and reconnect detection
- **Dark / Light Theme** — Persistent theme toggle stored in SharedPreferences
- **Cross-Platform** — Runs on Android, iOS, and Web (deployed to Firebase Hosting)

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Flutter 3.8+ (Dart) |
| State Management | GetX |
| Backend & Auth | Firebase Auth + Cloud Firestore |
| Places API | Geoapify |
| Location | geolocator, geocoding |
| Notifications | Awesome Notifications, WorkManager |
| Network | Dio, connectivity_plus |
| Local Storage | shared_preferences |
| Animations | flutter_animate |

---

## Getting Started

### Prerequisites

- Flutter SDK `^3.8.1`
- A [Firebase](https://console.firebase.google.com) project with **Authentication** (Email/Password) and **Firestore** enabled
- A [Geoapify](https://www.geoapify.com) API key

### Installation

```bash
git clone https://github.com/Marwan-Mohamed14/tour-guide-mobile-app.git
cd tour-guide-mobile-app
flutter pub get
```

Add your Firebase config by replacing `lib/firebaseoptions.dart` with the output from `flutterfire configure`, then add your Geoapify API key in the places service.

```bash
flutter run
```

---

## Usage

1. **Sign up or log in** with your email address
2. Grant **location permission** — the app discovers nearby places automatically
3. Browse places by **category** (museums, parks, restaurants, etc.)
4. Tap a place to see **details and Wikipedia info**
5. **Save favorites** or add a place to your **visit list** with a scheduled date
6. Receive a **notification reminder** on your visit day
7. Switch between **Arabic and English** in settings
