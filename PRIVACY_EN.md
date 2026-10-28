# Privacy Policy — MotoLink

**Last updated: 28 October 2026.**

This notice applies to the **MotoLink** Android app and to the features available in the installed version. MotoLink provides mirroring to compatible motorcycle displays, connection profiles and optional support features. The official privacy and support contact is **[motolinkofficial.app@gmail.com](mailto:motolinkofficial.app@gmail.com)**.

## Data and settings stored on the device

MotoLink stores motorcycle profiles, connection details configured or captured using QR codes, optional user-selected profile photos, favorite apps, interface and display-adjustment settings, preferences and technical logs locally.

The log may contain technical information about devices, motorcycles, networks, connections or errors. It remains on the phone until removed using **Support → Log → Clear → Clear Log**, by clearing the app's data or by uninstalling it. When the Assistant is used, anonymous session tokens are kept in the app's private storage. Saving a motorcycle profile does not by itself upload its details to the Assistant backend.

## Logs and diagnostics only on request

A normal Assistant conversation **does not automatically upload the log**.

- **External sharing:** the user chooses to open the Android share sheet and selects a recipient.
- **Sharing with the Assistant:** only when the user selects **Support → Log → Share → Assistant** is a filtered log extract (maximum 6,000 characters) prepared and voluntarily attached.

MotoLink applies local filtering and an additional server-side filter. These reduce the exposure of sensitive technical information but cannot guarantee removal of everything the user may have entered. **Do not send passwords, tokens, full codes or other confidential information.**

## MotoLink Assistant and anonymous sessions

The Assistant is optional and requires Internet access. When used, MotoLink creates an **anonymous technical session** through **Supabase Auth** without asking for a named user profile. The service stores the authentication information needed for the session.

- When **Send** is pressed, the HTTPS request may contain the question (up to 1,200 characters), the app version and, only if chosen by the user, filtered diagnostics.
- The backend can answer using the MotoLink knowledge base or request an answer from AI provider **Groq**.
- The MotoLink application database does not store chat history, questions, responses or the contents of logs sent to the Assistant. It keeps an aggregated daily count of AI-provider calls.

This statement does **not** exclude Supabase authentication records or technical metadata and infrastructure logs that service providers may handle under their respective terms.

## Mirroring, motorcycle connections, QR and navigation

- **Mirroring:** Android requests **MediaProjection** permission before screen capture. Visible content may include personal information or notifications. The stream is sent to the compatible motorcycle display over the local connection and is **not** uploaded to the Assistant backend.
- **Connection:** MotoLink uses Wi-Fi, Wi-Fi Direct/P2P and, where applicable, Bluetooth/BLE to connect to the motorcycle display; technical details may appear in local logs.
- **QR and camera:** pairing may use Google Code Scanner or the CameraX-based internal scanner as a fallback. Google services may process technical metadata under their policies.
- **Google Maps:** only after notification access is enabled, MotoLink interprets compatible Google Maps navigation notifications and sends directions to the display over BLE. This permission can be revoked in Android.

## External providers, PayPal and SOSTENITORE sticker

User-selected features may involve **Supabase** (authentication/backend), **Groq** (AI when needed), **Google/Android** (QR, system and navigation), **PayPal** (external donations) and the email app chosen by the user. Providers may handle IP addresses and other technical metadata under their terms.

PayPal donations are **voluntary**, with amounts chosen by the user, and do not unlock digital content or app features. Payment happens **outside MotoLink** on PayPal's website: the app does not directly collect card numbers or payment credentials. Some versions may load PayPal images or web resources on the Credits screen, causing technical requests to PayPal.

The optional **6 cm physical MotoLink SOSTENITORE sticker** is a **thank-you gift, not an in-app purchase**. Requesting it is not required to use MotoLink. If the user wishes to ask for it, their chosen email app opens: the user decides whether to send their first name, last name, delivery address and optional PayPal reference. If sent, this information is used to respond, manually check the donation and, when applicable, arrange delivery. MotoLink does not automatically transmit these details from the app.

Provider policies: [Supabase](https://supabase.com/privacy), [Groq](https://groq.com/privacy-policy/), [Google](https://policies.google.com/privacy), [PayPal](https://www.paypal.com/it/legalhub/paypal/privacy-full).

## Android permissions

Depending on the features used, MotoLink may request Internet/network status, Wi-Fi and nearby Wi-Fi devices, Bluetooth/BLE, camera for fallback QR scanning, legacy location on older Android versions, **MediaProjection**, foreground service, display over other apps and wake-lock/proximity capabilities. Google Maps notification access requires separate activation.

MotoLink does not request `QUERY_ALL_PACKAGES`: only launchable apps are displayed for favorites. Permissions can be reviewed or revoked in Android settings, which may limit the related features.

## Retention, deletion and privacy contact

- **Local data:** to clear the log use **Support → Log → Clear → Clear Log**. To remove motorcycle profiles, photos, settings and other local data, use **Android Settings → Apps → MotoLink → Storage → Clear data**, or uninstall the app.
- **Anonymous Assistant session:** in versions offering this option, select **Support → Log → Clear → Delete session** and confirm. The **tested** server function verifies the requested anonymous identity and deletes its Supabase record; on server confirmation the client clears its local tokens. This **does not** delete motorcycle profiles, settings or logs on the phone. Using the Assistant again may create a new anonymous session.
- **Outside the app:** visit **[MotoLink data deletion](https://mysterx92.github.io/motolink-privacy/delete-data.html)** or email **[motolinkofficial.app@gmail.com](mailto:motolinkofficial.app@gmail.com)**. Without an identifiable session, for example after uninstalling, it may not be technically possible to connect an emailed request with an anonymous identity. Never email tokens or passwords to request deletion.

Local data remains until the user clears it or deletes the app; the Supabase session remains until deletion. Retention of provider infrastructure logs and optional support/delivery correspondence depends on the respective systems and the handling of requests. Contact MotoLink at the address above for information, privacy rights requests or deletion enquiries. Deleting a Supabase identity does not automatically erase previously sent emails or independent provider records.
