# CineBox Android prototype

Native Android Kotlin + Jetpack Compose prototype for source selection and quality-aware playback.

## What works
- Source selection UI with Source A selected by default.
- Preferred quality starts at 4K.
- Quality options are only displayed if actual source metadata contains valid HTTPS renditions.
- SourceResolver selects the requested available rendition or falls back to the highest available rendition.
- Media3/ExoPlayer playback screen for configured authorized streams.
- No fake video URLs are bundled. Sources are empty by default, so playback stays disabled until a trusted backend/provider is configured.

## Build APK without a paid coding agent
1. Create a GitHub repository and upload these files.
2. Open the repository's Actions tab.
3. Run **Build CineBox APK** (or push to main/master).
4. Open the completed workflow run and download the `CineBox-debug-apk` artifact ZIP.
5. Extract `app-debug.apk` and install it on your Android phone. You may need to allow installation from that file manager.

## Local build
Requires JDK 17, Android SDK platform 35, and Gradle 8.9:
`gradle assembleDebug`

## Important
This is a functional UI/source-resolution prototype, not a populated streaming service. To enable playback, connect a backend that you own or are authorized to use and return actual HTTPS stream URLs plus rendition metadata. Do not hardcode or scrape private third-party APIs.
