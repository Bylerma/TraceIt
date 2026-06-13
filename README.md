# TraceIt - Lost & Found Application

TraceIt is a modern Android application designed to help users report and find lost or found items. Built with Material 3 design principles, it provides a seamless and user-friendly experience for community-driven item recovery.

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Tech Stack & Dependencies](#tech-stack--dependencies)
- [Project Structure](#project-structure)
- [Data Models](#data-models)
- [Setup & Build Instructions](#setup--build-instructions)
- [Firebase Configuration](#firebase-configuration)
- [Contributors](#contributors)

## Project Overview
- **App Name**: TraceIt
- **Type**: Native Android (Java)
- **Target**: Android 8.0+ (API 26+)
- **UI Theme**: Vibrant Indigo (#4361EE) & Teal (#4CC9F0) using Material 3.
- **Purpose**: Community-driven lost and found platform with location awareness and real-time chat.

## 🚀 Features
- **User Authentication**: Secure sign-up and login using Firebase Authentication (Email/Password & Google Sign-In).
- **Report Items**: Easily post lost or found items with photos, descriptions, categories, and locations (GPS).
- **Real-time Discovery**: Browse items in a dynamic staggered grid with real-time filtering and search.
- **Real-time Chat**: Connect directly with other users via an integrated chat system.
- **Interactive UI**: Modern Material 3 interface with smooth animations and responsive layouts.
- **Profile Management**: Manage your posts, track active/resolved items, and update your profile picture.

## 🛠️ Tech Stack & Dependencies
- **Language**: Java 11
- **UI Framework**: Android Material Components (Material 3), ViewBinding, ConstraintLayout.
- **Backend**: Firebase (Authentication, Firestore, Cloud Storage, Analytics).
- **Location**: Google Play Services Location.
- **Image Loading**: Glide.

## Project Structure
```
TraceIt/
├── app/
│   ├── src/main/
│   │   ├── java/com/lostandfound/
│   │   │   ├── activities/          # Splash, Login, SignUp, Main, AddPost, ItemDetail, Chat
│   │   │   ├── fragments/           # HomeFragment, MyPostsFragment, ProfileFragment
│   │   │   ├── adapters/            # ItemAdapter, MessageAdapter
│   │   │   ├── models/              # Item, User, Message
│   │   │   └── utils/               # FirebaseHelper, Constants, ImageUtils, DummyDataUtils
│   │   ├── res/
│   │   │   ├── layout/              # XML layouts for all screens
│   │   │   ├── drawable/            # Backgrounds, badges, chat bubbles
│   │   │   ├── anim/                # Slide & fade animations
│   │   │   └── values/              # strings, colors (vibrant theme), themes
│   │   └── AndroidManifest.xml
│   └── build.gradle
├── build.gradle
├── settings.gradle
└── README.md
```

## ⚙️ Setup & Build Instructions
1. **Clone the repository**:
   ```bash
   git clone https://github.com/Bylerma/Trace-t.git
   ```
2. **Open in Android Studio**: (Hedgehog or newer recommended).
3. **Connect Firebase**:
   - Add your `google-services.json` to the `app/` directory.
   - Enable Email/Password and Google sign-in methods in the Firebase Console.
4. **Configure SHA-1**:
   - Run the `./gradlew signingReport` task and add your SHA-1 fingerprint to the Firebase Project Settings.
5. **Update Web Client ID**:
   - Update `default_web_client_id` in `app/src/main/res/values/strings.xml` with your Firebase Web Client ID.
6. **Sync & Run**:
   - Click "Sync Project with Gradle Files" and run on an emulator or device (API 26+).

## Firebase Configuration
- **Authentication**: Enable Email/Password and Google providers.
- **Firestore**: Create a database in "Production" or "Test" mode.
- **Storage**: Set up rules to allow authenticated users to upload images to `item_images/` and `profile_avatars/`.

---

**TraceIt** – Helping communities reunite lost items with their owners. 🕵️‍♂️📍
