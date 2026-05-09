# Firebase Setup Instructions for Jetcity

## Step 1: Create Firebase Project
1. Go to https://console.firebase.google.com
2. Click "Add project"
3. Name it "Jetcity"
4. Click through the setup (disable Google Analytics is fine)
5. Wait for project creation

## Step 2: Enable Authentication
1. In Firebase Console, go to **Authentication**
2. Click **Get started**
3. Click **Email/Password**
4. Enable it and save

## Step 3: Get Your Config
1. In Firebase Console, click the gear icon (Settings)
2. Click **Project settings**
3. Scroll down to **Your apps** section
4. Click **Web** (or add it if not there)
5. Copy the config object that looks like:
```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "your-project.firebaseapp.com",
  projectId: "jetcity-xxxx",
  storageBucket: "jetcity-xxxx.appspot.com",
  messagingSenderId: "xxxxx",
  appId: "1:xxxxx:web:xxxxx"
};
```

## Step 4: Update the Config in auth.html
1. Open auth.html in the editor
2. Find the `firebaseConfig` object near the top of the `<script>` section
3. Replace it with YOUR config from Step 3
4. Save and commit to GitHub

Done! Your site now uses real Firebase auth that works across all devices.
