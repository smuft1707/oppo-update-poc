# Oppo Silent Install PoC (Insecure Deserialization)

This repository is for security research purposes only, specifically for a bug report on HackerOne.

## Components:
- `exploit.apk`: A dummy APK used to demonstrate silent installation.
- `index.html`: A malicious landing page that triggers the `oaps://` deep link.

## Vulnerability Flow:
1. User visits the GitHub Pages site.
2. User clicks the "Update" button.
3. The `com.heytap.market` app processes the intent.
4. The insecure deserialization in the `cb` parameter allows the attacker to trigger a silent installation of the downloaded APK.
