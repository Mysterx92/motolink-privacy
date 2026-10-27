# Privacy — MotoLink (English translation)

This page describes how MotoLink handles user data.

## Data stored on your phone

MotoLink may store locally:

- motorcycle profiles and related preferences;
- favorite apps;
- interface and display-adjustment settings;
- the state of features configured by the user;
- the MotoLink technical log.

The local log is not automatically deleted by the app. It remains available until you explicitly select **Clear** or clear the app's data.

## Logs and diagnostics

A normal conversation with the Assistant **does not automatically send the log**.

The log may leave the device only when you choose to:

- **Share externally**: Android opens the standard share sheet;
- **Send to Assistant**: MotoLink prepares filtered diagnostics and sends them together with your support request.

A local filter is applied before data is sent to the Assistant. The backend also applies a second server-side filter.

## MotoLink Assistant

To use the Assistant, MotoLink creates an anonymous technical session through Supabase Auth.

When you submit a question, the backend may receive:

- the text of the question;
- the app version;
- any filtered diagnostics you voluntarily attach.

Questions may be answered by the MotoLink knowledge base. When that is insufficient, the backend may use the configured AI model through an AI provider.

## Data not stored in the MotoLink application database

The architecture does not store in the MotoLink application database:

- chat history;
- question text;
- answer text;
- the contents of logs sent to the Assistant.

The backend maintains an aggregated technical counter consisting of the **day and number of AI-provider calls** to enforce the configured limit.

## Service providers

Supabase, AI providers, Android/Google and other services involved may process technical metadata or infrastructure logs under their respective terms and policies.

## Android permissions

Depending on the feature used, MotoLink may request permissions relating to:

- Internet and network status;
- location on older Android versions when required by legacy Wi-Fi APIs;
- MediaProjection (screen sharing);
- foreground services;
- displaying over other apps;
- wake locks and proximity features used by the app.

To let you choose your favorite apps, MotoLink displays only apps that can be launched from your phone.

## Deleting local data

Local data can be deleted through Android's app settings or by uninstalling MotoLink.
