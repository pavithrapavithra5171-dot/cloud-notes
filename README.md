☁️ Cloud Notes - A Secure Cloud-Based Note Taking Application
By Pavithra P | Final Year Project

<p align="center">
  <a href="https://pavithrapavithra5171-dot.github.io/cloud-notes/"><b>🌐 Live Website</b></a> •
  <a href="https://github.com/pavithrapavithra5171-dot/cloud-notes"><b>📂 GitHub Code</b></a> •
  <a href="#"><b>📱 APK Download</b></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Project-Final%20Year-blueviolet?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Live-success?style=for-the-badge">
  <img src="https://img.shields.io/badge/Firebase-Connected-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/PWA-Ready-blue?style=for-the-badge">
</p>

---

📖 About The Project

**Cloud Notes** is a modern, secure, and user-friendly note-taking application built for the cloud era. It allows users to create, edit, delete, and securely store their personal notes from anywhere, on any device.

Unlike traditional note apps that store data locally and risk data loss, Cloud Notes uses **Google Firebase** for real-time cloud synchronization and **AES Encryption** to ensure that user data remains private and secure even from database admins.

This project was developed as part of my Final Year Academic Project to demonstrate skills in Frontend Development, Backend Integration (BaaS), Cloud Security, and PWA Mobile App Development.

> **Tagline: Write Once, Access Anywhere, Secure Always.**

---

✨ Key Features

🔐 1. Secure User Authentication
- Firebase Email & Password Authentication
- User-specific data isolation
- Secure session management with auto-logout
- Password validation and error handling

🔒 2. End-to-End Encrypted Notes
- Notes are encrypted using **AES (Advanced Encryption Standard)** before saving to cloud
- Decrypted only on user's device when viewing
- Even Firebase console shows only encrypted text
- Ensures complete privacy

☁️ 3. Real-Time Cloud Sync
- Powered by **Firebase Firestore**
- Notes sync instantly across all devices
- No data loss on phone change or uninstall
- Offline support - notes cached locally and synced when online

📝 4. Complete Note Management (CRUD)
- **Create:** Rich text notes with title and content
- **Read:** View all notes in beautiful card layout
- **Update:** Edit existing notes instantly
- **Delete:** Secure deletion with confirmation
- Timestamps: Created at & Updated at tracking

🔍 5. Smart Search & Organization
- Instant search - Search by title or content
- Real-time filtering as you type
- Clean, minimal, distraction-free UI

🎨 6. Beautiful & Responsive UI
- Modern Purple Gradient Theme - Designed for focus and calm
- Fully Responsive - Works on Mobile, Tablet, Desktop
- Poppins Font & Material Icons
- Smooth animations and transitions

📱 7. PWA & APK Ready
- Progressive Web App - Can be installed on any phone
- APK Generated - Works like native Android app
- No Play Store needed
- Lightweight and fast

---

🛠️ Technology Stack

| Category | Technology Used |
| :--- | :--- |
| **Frontend** | HTML5, CSS3, JavaScript (ES6+) |
| **Styling** | Custom CSS, Flexbox, Grid, Gradients |
| **Backend (BaaS)** | Google Firebase |
| **Authentication** | Firebase Auth (Email/Password) |
| **Database** | Cloud Firestore (NoSQL) |
| **Security** | AES Encryption (CryptoJS), Firebase Security Rules |
| **Hosting** | GitHub Pages & Firebase Hosting |
| **Mobile App** | PWA (Progressive Web App) - APK Build |
| **Version Control** | Git & GitHub |

---

🏗️ Architecture & Workflow

User (Browser/APK) -> Login (Firebase Auth) -> Token Verification
-> Create Note -> AES Encrypt -> Save to Firestore (UserID)
-> Read Notes -> Fetch Encrypted Data -> AES Decrypt -> Display

1.  User Registers / Logs in via Firebase Auth
2.  Firebase returns a secure UID
3.  All notes are stored under `users/{UID}/notes`
4.  Before saving, content is encrypted in the browser
5.  On retrieval, content is decrypted in the browser only

---

🔒 Security Model

This project implements 3-layer security:

1.  **Firebase Authentication:** Only authenticated users can access app.
2.  **Firestore Security Rules:** 
    ```javascript
    match /users/{userId}/{document=**} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
Means: A user can ONLY access their own notes.
3.  *Client-Side AES Encryption:* Notes content is encrypted before upload, so even if database is leaked, notes are unreadable without key.

---

🚀 Live Links

- *🌐 Live Website:* https://pavithrapavithra5171-dot.github.io/cloud-notes/
- *📂 GitHub Repository:* https://github.com/pavithrapavithra5171-dot/cloud-notes
- *🔥 Firebase Console:* (Private - Connected via http://config.json)

---

💻 How to Run Locally

Prerequisites
- Any modern browser (Chrome recommended)
- Firebase Account

Steps

1.  *Clone the repository*
    git clone https://github.com/pavithrapavithra5171-dot/cloud-notes.git
    cd cloud-notes
2.  *Firebase Setup (Already configured)*
    - `config.json` contains Firebase keys
    - If you want to use your own Firebase, replace keys in `config.json`

3.  *Run the app*
    - Simply open `index.html` in browser
    - Or use VS Code Live Server extension for best experience

4.  *Create Account & Use*
    - Click Create New Account
    - Login and start creating notes!

---

📂 Folder Structure
cloud-notes/
│
├── index.html          # Main HTML - Login, Register, Dashboard UI
├── app.js              # Core Logic - Auth, CRUD, Search, Encryption
├── style.css           # Complete Styling - Purple Theme, Responsive
├── config.json         # Firebase Configuration Keys
├── manifest.json       # PWA Manifest - App name, icons, theme
├── sw.js               # Service Worker (for offline support)
├── README.md           # Project Documentation (This file)
└── assets/             # (Optional) Screenshots & Icons
---

🎯 Future Enhancements

- [ ] Rich Text Editor (Bold, Italic, Lists)
- [ ] Categories / Tags / Folders for notes
- [ ] Pin / Favorite Notes
- [ ] Dark Mode / Light Mode Toggle
- [ ] Share Notes via Link
- [ ] Voice Notes & Image Attachments
- [ ] Reminder / To-Do Checklist Integration

---

👩‍💻 Author

*Pavithra P*
- Final Year Student
- Bangalore, Karnataka, India
- GitHub: https://github.com/pavithrapavithra5171-dot

*Project Guide:* Respected Faculty
*Academic Year:* 2025-2026

---

🙏 Acknowledgements

- Google Firebase for amazing Backend-as-a-Service
- CryptoJS for AES Encryption library
- GitHub Pages for free hosting
- Inspiration from Google Keep & Notion

---

📜 License

This project is developed for educational purposes - Final Year Academic Project.
Feel free to fork and learn!

---

<p align="center">⭐ Star this repo if you found it helpful! ⭐</p>
<p align="center">Made with 💜 by Pavithra</p>

---
