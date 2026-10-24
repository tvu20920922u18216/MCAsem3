# 📚 Exam Preparation Portal

A lightweight, single-file web application designed to help students prepare for exams (AML, AJP, Web Development) with 2, 5, and 10-mark questions. It features a dual-mode interface (Study & Admin), smart text formatting, and **global cloud PDF storage** powered by Firebase.

## ✨ Features

### 📖 For Students (Study Mode)
- **Subject & Unit Filtering**: Easily navigate through AML, AJP, and Web Development units.
- **Marks Filter**: Filter questions by 2, 5, or 10 marks.
- **Smart Search**: Instantly search through questions and answers.
- **PDF Resource Hub**: View and download study materials uploaded by admins directly in the browser.
- **Built-in PDF Viewer**: Read PDFs without leaving the website.
- **Export to PDF**: Generate and download a PDF of the current unit's questions.

### ⚙️ For Administrators (Admin Mode)
- **Secure Login**: Password-protected admin dashboard (default: `admin123`).
- **Easy Question Import**: 
  - Simple Text (auto-formats bullets, bold, and paragraphs).
  - Bulk Paste (one question/answer per line).
  - CSV/Excel Upload.
- **Step-by-Step Editor**: Intuitive UI to find, edit, or delete specific questions.
- **Cloud PDF Management**: Upload PDF files directly to Firebase Cloud Storage, making them instantly visible to **all users globally**.
- **Data Backup**: Export all question data as a JSON file.

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript (No frameworks required)
- **Backend / Cloud**: Firebase (Firestore Database & Cloud Storage)
- **Libraries**: 
  - [jsPDF](https://github.com/parallax/jsPDF) (for generating question PDFs)
  - Firebase SDK v8 (for cloud storage and database)

---

## 🚀 Setup & Installation

Since this is a single-file application, setup is incredibly easy. However, to enable **global PDF uploads**, you must connect it to a free Firebase project.

### Step 1: Create a Free Firebase Project
1. Go to the [Firebase Console](https://console.firebase.google.com/).
2. Click **Add project** and follow the setup wizard (you can disable Google Analytics).
3. Once created, click on the project.

### Step 2: Enable Firestore Database
1. In the left sidebar, go to **Build** > **Firestore Database**.
2. Click **Create database**.
3. Choose a location closest to you.
4. Select **Start in test mode** (this allows read/write access for development). Click **Enable**.

### Step 3: Enable Cloud Storage
1. In the left sidebar, go to **Build** > **Storage**.
2. Click **Get started**.
3. Select **Start in test mode** and click **Enable**.

### Step 4: Get Your Firebase Configuration
1. Click the ⚙️ **Gear icon** (Project Settings) at the top left of the sidebar.
2. Scroll down to the "Your apps" section and click the **`</>` (Web)** icon.
3. Register the app with a nickname (e.g., `ExamPrepWeb`).
4. Copy the `firebaseConfig` object provided. It will look like this:
   ```javascript
   const firebaseConfig = {
     apiKey: "AIzaSy...",
     authDomain: "your-project.firebaseapp.com",
     projectId: "your-project",
     storageBucket: "your-project.appspot.com",
     messagingSenderId: "123456789",
     appId: "1:123456789:web:abcdef"
   };
