# Pool Cost Calculator — iPhone Installation

This package is a Progressive Web App (PWA). It behaves like an iPhone app, has its own Home Screen icon, and works offline after the first successful launch.

## Fastest setup: GitHub Pages

1. Create a new public GitHub repository, for example `pool-cost-calculator`.
2. Upload all files and folders from this ZIP to the repository root.
3. Open the repository's **Settings**.
4. Select **Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select the `main` branch and `/ (root)`, then save.
7. GitHub will provide an HTTPS website address.

## Install on iPhone

1. Open the published website address in **Safari**.
2. Tap the **Share** button.
3. Tap **Add to Home Screen**.
4. Keep **Open as Web App** enabled when shown.
5. Tap **Add**.

The Pool Cost icon will appear on the Home Screen. Open it once while connected to the internet so all offline files are cached.

## Files

- `index.html` — calculator interface and formulas
- `manifest.webmanifest` — app name, appearance, and icons
- `service-worker.js` — offline support
- `icons/` — iPhone and PWA icons

## Formula logic

Option 1:
`Total = (50 × N) + (0.5 × B)`

Option 2:
- When `B < 75 × N`: `Total = 75 × N`
- When `B ≥ 75 × N`: `Total = (75 × N) + (B − 75 × N)`

Where:
- `N` = number of people
- `B` = total food and beverage bill
