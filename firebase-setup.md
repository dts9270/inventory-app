Firebase Quick Setup (what to enable)
------------------------------------
1) Authentication:
   - In Firebase Console -> Authentication -> Sign-in method -> Enable Phone.

2) Firestore:
   - Create Firestore database in Native mode.
   - Create collection 'admins' and add a document with ID '+917020970727'
     Example document fields:
     {
       "phone": "+917020970727",
       "role": "admin",
       "createdAt": <timestamp>
     }

3) Storage:
   - Enable Firebase Storage (default rules ok for testing).
   - For production, set rules to require authentication:
     rules_version = '2';
     service firebase.storage {
       match /b/{bucket}/o {
         match /{allPaths=**} {
           allow read, write: if request.auth != null;
         }
       }
     }

4) Firestore rules (basic):
   rules_version = '2';
   service cloud.firestore {
     match /databases/{database}/documents {
       match /{document=**} {
         allow read, write: if request.auth != null;
       }
     }
   }

5) Authorized domains:
   - Add your GitHub Pages domain (<your-username>.github.io) and localhost.

6) Testing:
   - Use the app on your live GitHub Pages URL after uploading.
