<p align="center">
  <a href="https://amplitude.com" target="_blank" align="center">
    <img src="https://static.amplitude.com/lightning/46c85bfd91905de8047f1ee65c7c93d6fa9ee6ea/static/media/amplitude-logo-with-text.4fb9e463.svg" width="280">
  </a>
  <br />
</p>

# Amplitude Session Replay Flutter SDK

> **Warning**
> This SDK is currently in alpha. APIs may change and there will be breaking changes before the stable release.

This is Amplitude's Session Replay SDK for Flutter.

## Installation

Add the package to your `pubspec.yaml`:

```yaml
dependencies:
  amplitude_session_replay: ^0.0.1-alpha.1
```

Then run:

```bash
flutter pub get
```

## Quick Start

Wrap your app with `SessionReplayWidget`:

```dart
import 'package:amplitude_session_replay/amplitude_session_replay.dart';

void main() async {
  WidgetsFlutterBinding.ensureInitialized();

  final config = SessionReplayConfig(
    apiKey: 'YOUR_AMPLITUDE_API_KEY',
    deviceId: 'your-device-id',
    sessionId: 123456789, // from your analytics SDK
  );

  runApp(SessionReplayWidget(config: config, app: const MyApp()));
}
```

## Need Help?

If you have any problems or issues over our SDK, feel free to [create a GitHub issue](https://github.com/amplitude/AmplitudeSessionReplay-Flutter/issues/new) or submit a request on [Amplitude Help](https://help.amplitude.com/hc/en-us/requests/new).
