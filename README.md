# 🚨 SafeVoice (SIPA)
### Smart Emergency Protection Assistant

SafeVoice (SIPA) is a **real-time safety and emergency response system** designed to assist users in dangerous situations.  
The system combines a **React Native mobile application** and a **web-based monitoring dashboard** to detect emergencies, track user location, alert contacts, and preserve evidence.

This project uses **voice recognition, real-time GPS tracking, Firebase cloud services, and background monitoring** to provide immediate assistance during emergencies.

---

# 🌐 Live Web Dashboard

The SafeVoice web monitoring dashboard is deployed using **GitHub Pages**.

🔗 **Live Website**  
https://rohitmunnuru9.github.io/ASAFE/

This dashboard allows responders or trusted contacts to **monitor emergency sessions and trigger SOS alerts**.

---

# 🏗️ System Architecture

SafeVoice consists of **two primary components**:

## 1️⃣ Mobile Application – SafeVoice
Built using **React Native**, the mobile application is responsible for:

- Detecting emergency triggers
- Capturing location data
- Recording evidence
- Sending alerts
- Syncing data with the cloud

## 2️⃣ Web Dashboard – safevoice-web

The web dashboard provides a **real-time monitoring interface** for emergency responders or trusted contacts.

Features include:

- Live location tracking
- Emergency session monitoring
- Manual SOS activation
- Quick contact communication

---

# 🚀 Key Features

## 🔴 Emergency Triggers

SafeVoice supports **multiple ways to activate emergency mode**.

### 1. SOS Button
- Large central button for immediate emergency activation
- Designed for **quick access during stressful situations**

### 2. Voice Activation
Uses **Picovoice Porcupine** for wake-word detection.

Example trigger phrase:

```
Help Me Now
```

Works even when:

- Phone screen is locked
- App is running in the background

### 3. Gesture Trigger
- Emergency activation using **5-tap gesture**
- Useful when users cannot interact normally with the phone

---

# ⚡ Automatic Emergency Actions

Once triggered, SafeVoice automatically performs several safety actions.

## 📍 Live Location Tracking
- High-accuracy GPS tracking
- Location updates every few seconds
- Stored in **Firebase Firestore**

## 📩 Emergency Alerts
The system automatically:

- Generates a **Google Maps location link**
- Opens the default **SMS app**
- Sends emergency alerts to trusted contacts

## 🔊 Alarm Siren
- Loud siren designed to **deter attackers**
- Can be configured as **silent alarm mode**

## 📞 Fake Call Feature
- Simulates an incoming call
- Helps users **exit uncomfortable situations safely**

---

# 🎥 Evidence Collection

SafeVoice automatically records potential evidence during emergencies.

## Silent Camera Recording

Using **Vision Camera**, the app:

- Records video/audio silently
- Works even in background
- Stores footage securely

Evidence can be uploaded to **Firebase Storage** for future reference.

---

# 📡 Real-Time Monitoring

The **SafeVoice Web Dashboard** allows live tracking of emergency situations.

### Dashboard Features

- Live GPS tracking
- Emergency session visualization
- SOS trigger button
- Direct call and message options

### UI Design

The dashboard uses a **premium glassmorphism interface** including:

- Dark theme
- Smooth animations
- High contrast emergency controls

---

# 🧰 Technology Stack

## Mobile Application
- React Native
- Picovoice Porcupine
- Vision Camera
- React Native Background Actions

## Backend Services
- Firebase Authentication
- Firebase Firestore
- Firebase Storage

## Web Dashboard
- React / Web Technologies
- GitHub Pages Deployment
- Glassmorphism UI

---

# 📁 Project Structure

```
src
 ├── services
 │   ├── AlertManager.js
 │   ├── TriggerService.js
 │   └── CameraService.js
 │
 ├── screens
 │   ├── DashboardScreen.js
 │   └── SettingsScreen.js
 │
 ├── styles
 │   └── theme.js
```

### Core Modules

**AlertManager.js**  
Handles the orchestration of emergency actions.

**TriggerService.js**  
Responsible for detecting voice wake-word triggers.

**CameraService.js**  
Manages silent camera recording and uploads.

**DashboardScreen.js**  
Main UI screen containing the SOS button.

**SettingsScreen.js**  
Allows users to configure safety features.

---

# 🔄 Emergency Workflow

## Step 1 — Detection

Emergency can be triggered via:

- Voice command
- SOS button
- Gesture activation

---

## Step 2 — Activation

The system:

- Creates a unique **emergency session**
- Stores it in **Firebase Firestore**
- Starts **high-accuracy GPS tracking**

---

## Step 3 — Alerting

SafeVoice then:

- Generates a **Google Maps location link**
- Opens **SMS application**
- Sends alerts to emergency contacts

---

## Step 4 — Monitoring

- Location updates are pushed to **Firebase**
- Dashboard shows **live movement of the user**

---

## Step 5 — Evidence Preservation

- Camera recording begins silently
- Video logs are uploaded to **Firebase Storage**

---

# ⚙️ Setup and Configuration

## 1️⃣ Clone Repository

```
git clone https://github.com/rohitmunnuru9/ASAFE.git
cd ASAFE
```

---

## 2️⃣ Install Dependencies

```
npm install
```

or

```
yarn install
```

---

## 3️⃣ Firebase Setup

Create a Firebase project and add configuration files.

### Android

```
android/app/google-services.json
```

### iOS

```
ios/GoogleService-Info.plist
```

---

## 4️⃣ Picovoice Setup

1. Create account at **Picovoice Console**
2. Generate an **Access Key**
3. Replace placeholder in

```
App.tsx
```

Example:

```javascript
const PICOVOICE_ACCESS_KEY = "YOUR_ACCESS_KEY";
```

---

## 5️⃣ Run Application

### Android

```
npx react-native run-android
```

### iOS

```
npx react-native run-ios
```

---

# 🔐 Required Permissions

The app requests the following permissions:

- Microphone
- Location
- Camera
- Storage

These permissions are required for emergency detection and evidence recording.

---

# ✅ Verification Results

### Project Initialization
Successfully initialized **React Native 0.84.1**

### Dependency Integration
Installed and linked:

- Firebase
- Picovoice
- Vision Camera
- Background services

### UI/UX
Implemented:

- Premium dark mode
- Smooth animations
- Responsive layouts

### Emergency Flow
Verified full SOS workflow:

```
Trigger → Alert → GPS Tracking → Evidence Recording
```

---

# 🎥 Demonstration

(Add screenshots or demo video here)

Example:

```
/demo/mobile-app.png
/demo/dashboard.png
/demo/emergency-flow.png
```

---

# 🔮 Future Improvements

- Automatic SMS sending
- AI-based threat detection
- Smart wearable integration
- Offline emergency caching
- Integration with police/emergency APIs

---

# 📜 License

This project was developed as part of the **SIP (Software Innovation Project)**.

It is intended for **research, educational, and safety application development purposes**.

---

# 👨‍💻 Author

**Rohit Munnuru**

GitHub  
https://github.com/rohitmunnuru9

Live Project  
https://rohitmunnuru9.github.io/ASAFE/

---
