# LSRO PVP Tournament

This repository hosts the LSRO PVP tournament manager.

## Firebase setup

1. Create a Firebase Web app and Firestore database in project `lsro-pvp-tournament`.
2. In Firebase Authentication, enable **Email/Password** and create an account for the tournament manager and each authorized staff member.
3. In Firestore → Rules, publish the contents of `firestore.rules`. These rules require a signed-in Firebase user; do not use public read/write rules.
4. Deploy the web app using GitHub Pages (Settings → Pages → Deploy from branch → `main` / `/(root)`).

## Important status

The Firebase configuration is specific to this project. The tournament HTML still needs to be added to the repository and verified end-to-end before the site is ready for staff use. Do not share Firebase account passwords or service-account private keys.

## Shared roster behavior

The web app should sign users in with Firebase Authentication and store the roster in the Firestore document `tournaments/shared-roster`. Only authenticated users can access this document under the provided rules.
