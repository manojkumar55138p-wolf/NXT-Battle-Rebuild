# NXT Battle Rebuild

A clean-room Android rebuild starter based on the supplied reference APK's observable UI and assets. The project does not contain the original APK's signing keys, private credentials, backend secrets, or payment secrets.

## Included
- Home, Games, Wallet, Profile and Transactions screens
- Add Money flow
- PhonePe / UPI Intent entry
- Google Pay / UPI Intent entry
- UPI QR payment screen with replaceable merchant QR asset
- Payment verification placeholder designed for server-side verification
- Persistent demo wallet balance storage
- Portrait Android app with no third-party runtime dependency

## Before production
1. Replace `YOUR_VPA@upi` in `MainActivity.java` with the merchant VPA only after the payment architecture is finalized.
2. Replace the QR placeholder with the merchant QR image supplied by the owner.
3. Add a secure backend for payment order creation, webhook handling, UTR verification and wallet ledger updates.
4. Never credit wallet balance solely from a client-side callback.
5. Add authentication, server-backed user accounts, match APIs and game result APIs.

## Build
Open this folder in Android Studio and let Gradle sync. Run the app on an Android phone or emulator.


## Merchant QR
The supplied merchant QR is included as `app/src/main/res/drawable/merchant_upi_qr.png` and is displayed in the UPI QR payment screen. The encoded UPI payment address is used by the UPI intent flow. Real wallet credit still requires server-side payment verification.
