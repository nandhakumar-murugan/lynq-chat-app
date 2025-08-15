# LYNQ-Chat-App

📱 LYNQ – A Privacy-First, Smart Messaging App
LYNQ is an end-to-end encrypted, cross-platform messaging application built to redefine secure and intelligent communication. It combines cutting-edge cryptography, real-time communication, and AI-powered features to ensure not just privacy but also a smarter user experience. Designed for mobile platforms, LYNQ empowers users to communicate securely, lookup word meaning and verify shared content.

🚀 Features
🔐 Basic Features:
Real-Time Chat – Send and receive messages instantly with WebSockets.

End-to-End Encryption – All messages are protected using X25519 (Key Exchange), ChaCha20-Poly1305(AEAD) and Poly1305 (MAC).

User Authentication – Secure login and registration system using Firebase Auth.

Auto-Link Verification – Links shared in messages are automatically scanned for phishing or malicious content.

Media Sharing – Securely share images and files within chat.

Group Chats – Encrypted group chat support with synchronized messages.


📡 Advanced Features:

Auto-Blocks Unsafe Links – If a malicious link is detected, the link can be blocked until the user approves it.
Word Lookup - Lookup for word meanings within the chat itself.
Realtime Translation to English - Translate a message of a different language to english for understanding.


🧠 How It Works
User Signup/Login:

Generates identity and encryption keys.

Authenticates with backend using hashed credentials andFirebase.

Start a Conversation:

Requests the receiver's pre-keys from the server.

Uses E2EE to establish a secure session.

Send a Message:

Message is encrypted on the client side.

Optionally scanned for unsafe links.

Sent to server and relayed to the receiver.

Receive Message:

Decrypted locally using session keys.



🔒 Security Highlights
Uses X25519 (Key Exchange), ChaCha20-Poly1305(AEAD) and Poly1305 (MAC) for true end-to-end encryption.

All messages are encrypted before leaving the device.

No messages are stored in plaintext, even on the server.

Implements forward secrecy, ensuring past messages stay secure even if current keys are compromised.

Auto-blocks malicious messages until user approval based on threat detection APIs.



📱 Supported Platforms

Mobile : Planned support via React Native


🤝 Team
	Mirdula R
	Piriyadharshini L K
 	Tayanithaa N S
  	Logesh Raj B
   	Jaisurya S
