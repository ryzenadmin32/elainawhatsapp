# ELAINAWHATSAPP

Static HTML app using Firebase Authentication + Cloud Firestore + WebRTC signaling.

## Deploy to Vercel from a phone
1. Extract this ZIP.
2. Create a new GitHub repository.
3. Upload `index.html`, `firestore.rules`, and `vercel.json` to the repository root.
4. In Vercel, choose **Add New → Project**, import that GitHub repository, then deploy.
5. In Firebase Console → Authentication → Settings → Authorized domains, add the exact `*.vercel.app` domain Vercel gives you.
6. In Firebase Console → Firestore Database → Rules, publish the contents of `firestore.rules`.

## Important
- This is a WhatsApp-inspired independent app, not the official WhatsApp app.
- Email/Password must be enabled in Firebase Authentication and Firestore must be created.
- Do not use open rules such as `allow read, write: if true`.
- Test with two different accounts and keep the Firestore rules enabled.
- Audio/video calling requires browser camera/microphone permissions and HTTPS. WebRTC calling can need TURN infrastructure for some networks; the included STUN servers are not enough for every network.
- The HTML contains the Firebase web app config. Firebase web config is not a server secret; Firestore Security Rules and API restrictions are important.
