# JONAKI AI — Voice Assistant

A native Android Java starter project for a voice-operated phone assistant. It contains no AI API key or API endpoint.

## Included
- Bengali speech recognition through the Android speech-recognition service.
- Android Text-to-Speech replies.
- Visible foreground microphone service, started by the user, with an ongoing notification.
- Basic commands for opening YouTube, searching YouTube, opening/searching Play Store, WhatsApp, TikTok, Android Settings, and telling the time.
- Dark neon UI and vector app icon.
- GitHub Actions workflow that builds a debug APK.

## Important platform limitations
- This is a command-based assistant, not a general AI model. It only understands the commands implemented in `VoiceAssistantService.java`.
- Female voice is not guaranteed by Android APIs. It uses the phone's installed Bengali TTS voice; install/select a female Bengali voice in Android Text-to-Speech settings if your device offers one.
- Continuous listening is started only after the user taps START LISTENING while the app is visible. Android displays an ongoing microphone notification. Tap STOP LISTENING in the app to stop. Android, battery saver, or the speech-recognition provider may still interrupt recognition; uninterrupted listening cannot be guaranteed.
- Voice recognition may require internet depending on the speech service and language pack.
- Play Store installation, WhatsApp message sending, TikTok/YouTube uploads and publishing are not silently automated. The app opens the relevant app/page; the user must review and confirm sensitive actions.
- WhatsApp currently opens the app; it does not identify a contact or send a message automatically.
- No accessibility service is included.

## Build
1. Create a new GitHub repository.
2. Extract this ZIP and upload its **contents** to the repository root. Do not upload the ZIP as one file or nest the project folder.
3. Include the hidden `.github/workflows/android.yml` file.
4. Open Actions and run **Build JONAKI AI APK**.
5. Download artifact `JONAKI-AI-APK` from a successful run and extract `app-debug.apk`.

Build success has not been independently verified in this environment. If GitHub Actions fails, share the complete first error block from the build log.
