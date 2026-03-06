# AnimatedOpacity Demo

A Flutter app demonstrating the `AnimatedOpacity` widget — a built-in implicit animation widget that smoothly transitions a widget's opacity between two values over a set duration.

---

## How to Run

**Prerequisites:** Flutter SDK installed and a browser available.

```bash
flutter pub get
flutter run -d chrome
```

The app opens in Chrome. Tap **Show** to fade the card in, tap **Hide** to fade it out.

---

## Widget: AnimatedOpacity

`AnimatedOpacity` wraps any widget and automatically animates changes to its opacity without requiring an animation controller.

### The three key attributes used in this app

| Attribute | Type | Description |
|-----------|------|-------------|
| `opacity` | `double` (0.0 – 1.0) | The target opacity. `1.0` is fully visible, `0.0` is fully transparent. Changing this value triggers the animation. |
| `duration` | `Duration` | How long the fade animation takes. Set to `500ms` in this app. |
| `child` | `Widget` | The widget whose visibility is being animated. Can be any widget — text, image, card, etc. |

### Usage in this app

```dart
AnimatedOpacity(
  opacity: _visible ? 1.0 : 0.0,       // driven by a single bool
  duration: const Duration(milliseconds: 500),
  child: Container(/* the card */),
)
```

---

## Screenshot

![App UI](screenshots/ui.png)

---

## Project Structure

```
lib/
  main.dart       # entire app — MyApp, MyHomePage, _MyHomePageState
screenshots/
  ui.png          # final UI screenshot
```
