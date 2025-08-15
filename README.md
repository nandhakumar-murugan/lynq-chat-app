# LYNQ-Chat-App

📱 LYNQ – A Privacy-First, Smart Messaging App
LYNQ is an end-to-end encrypted, cross-platform messaging application built to redefine secure and intelligent communication. It combines cutting-edge cryptography, real-time communication, and AI-powered features to ensure not just privacy but also a smarter user experience. Designed for mobile platforms, LYNQ empowers users to communicate securely, lookup word meaning and verify shared content.

---

## 🚀 Project Status (As of August 15, 2025)

This project is currently in the initial setup phase. Here's a summary of what has been completed:

*   **Project Initialization:** A new React Native project has been created in the `LYNQChatApp` directory.
*   **Firebase Integration:**
    *   The core Firebase dependencies (`@react-native-firebase/app` and `@react-native-firebase/auth`) have been added to the project.
    *   The native Android project has been configured to connect with Firebase. The `build.gradle` files have been updated, and the `google-services.json` file has been added.

### 🚨 Current Blockers
The project is currently **not buildable** due to a local environment configuration issue.
1.  **Android SDK Location:** The build will fail until the local path to the Android SDK is correctly configured.
2.  **Emulator/Device:** An Android emulator must be running or a physical device must be connected to launch the application.

---

## 🛠️ Development Setup

Follow these steps to get the development environment up and running.

### Prerequisites
*   Node.js
*   Java Development Kit (JDK)
*   Android Studio & Android SDK

### 1. Clone the Repository
```bash
git clone <repository-url>
cd LYNQ-Chat-App-main
```

### 2. Install Dependencies
Navigate to the React Native project directory and install the required npm packages.
```bash
cd LYNQChatApp
npm install
```

### 3. Configure Android SDK
This is a critical step to resolve the current build error.
1.  Create a new file named `local.properties` inside the `LYNQChatApp/android` directory.
2.  Open the `local.properties` file and add the following line, **replacing `path/to/your/android/sdk` with the actual path to your Android SDK**:
    ```
    sdk.dir=path/to/your/android/sdk
    ```
    *Example on Windows:* `sdk.dir=C:\\Users\\YourUsername\\AppData\\Local\\Android\\Sdk`
    *Example on macOS:* `sdk.dir=/Users/YourUsername/Library/Android/sdk`

### 4. Run the Application
1.  Open Android Studio and start an Android emulator, or connect a physical Android device to your computer.
2.  Run the following command from the `LYNQChatApp` directory to build and launch the app:
    ```bash
    npx react-native run-android
    ```
---📁 Project Structure
LYNQChatApp/
├── src/
│   ├── api/              # For external API calls (e.g., link verification, translation)
│   ├── assets/           # For images, fonts, and other static assets
│   ├── components/       # For reusable UI components
│   ├── config/           # For configuration files (e.g., Firebase config)
│   ├── features/         # For feature-specific code
│   │   ├── auth/         # For authentication-related code
│   │   ├── chat/         # For real-time chat functionality
│   │   ├── linkVerification/ # For link scanning and verification
│   │   ├── media/        # For media sharing functionality
│   │   ├── translation/  # For real-time translation
│   │   └── wordLookup/   # For word lookup functionality
│   ├── navigation/       # For screen navigation and routing
│   ├── screens/          # For the main screens of the app
│   ├── services/         # For core services (e.g., encryption, WebSocket)
│   └── utils/            # For utility functions and helpers

## 📝 Original App Concept

### Features
🔐 **Basic Features:**
*   **Real-Time Chat** – Send and receive messages instantly with WebSockets.
*   **End-to-End Encryption** – All messages are protected using X25519 (Key Exchange), ChaCha20-Poly1305(AEAD) and Poly1305 (MAC).
*   **User Authentication** – Secure login and registration system using Firebase Auth.
*   **Auto-Link Verification** – Links shared in messages are automatically scanned for phishing or malicious content.
*   **Media Sharing** – Securely share images and files within chat.
*   **Group Chats** – Encrypted group chat support with synchronized messages.

📡 **Advanced Features:**
*   **Auto-Blocks Unsafe Links** – If a malicious link is detected, the link can be blocked until the user approves it.
*   **Word Lookup** - Lookup for word meanings within the chat itself.
*   **Realtime Translation to English** - Translate a message of a different language to english for understanding.

### How It Works
*   **User Signup/Login:** Generates identity and encryption keys. Authenticates with backend using hashed credentials and Firebase.
*   **Start a Conversation:** Requests the receiver's pre-keys from the server. Uses E2EE to establish a secure session.
*   **Send a Message:** Message is encrypted on the client side. Optionally scanned for unsafe links. Sent to server and relayed to the receiver.
*   **Receive Message:** Decrypted locally using session keys.

### Security Highlights
*   Uses X25519 (Key Exchange), ChaCha20-Poly1305(AEAD) and Poly1305 (MAC) for true end-to-end encryption.
*   All messages are encrypted before leaving the device.
*   No messages are stored in plaintext, even on the server.
*   Implements forward secrecy, ensuring past messages stay secure even if current keys are compromised.
*   Auto-blocks malicious messages until user approval based on threat detection APIs.

### Supported Platforms
*   **Mobile:** Planned support via React Native

---

### 🤝 Team
*   Mirdula R
*   Piriyadharshini L K
*   Tayanithaa N S
*   Logesh Raj B
*   Jaisurya S
