Inventory App (GitHub Pages) - Ready to Upload
===============================================

What this package contains:
- index.html : Single-file mobile-friendly app (Marathi) using Firebase (Phone OTP, Firestore, Storage)
- No build required — upload these files to GitHub Pages as-is.

How to publish on GitHub Pages (mobile):
1. Create a new GitHub repository named `inventory-app`.
2. Open the repo and tap "Add file" → "Upload files".
3. Unzip the ZIP you downloaded and upload all files (index.html and any folders).
4. Commit changes to `main` branch.
5. Go to repo Settings → Pages → Select source: Branch `main`, folder `/` (root) → Save.
6. After a minute, your site will be live at https://<your-github-username>.github.io/inventory-app/

Firebase setup:
- You already provided firebaseConfig; ensure Firestore, Storage, and Authentication (Phone) are enabled.
- For admin access, create a document in Firestore:
  Collection: admins
  Document ID: +917020970727
  Fields: { role: "admin", phone: "+917020970727", createdAt: <timestamp> }

Notes:
- The app uses Firebase compat SDK via CDN — fine for small, private usage.
- For production usage, secure Firestore/Storage rules and consider restricting access.
- If you want me to deploy to GitHub for you, provide GitHub access (not recommended). Instead, upload the files yourself — it's simple and private.

If you want additions (analytics, stronger security rules, editing entries, delete protections), tell me and I'll update the package.
