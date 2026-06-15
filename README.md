# Bigfoot Trailers — Windows Releases

Public download & automatic-update feed for the **Bigfoot Trailers — Production
Management** Windows desktop app. The application source code lives in a
separate private repository; only the built, signed installers are published
here so they can be downloaded without a GitHub account.

The app connects to the live server at `https://bigfoot-trailers.duckdns.org` —
sign in with the account you were given.

## Install (recommended — auto-updates)

1. **Trust the app certificate** (one time, per machine, needs an administrator).
   Download [`BigfootTrailers.cer`](https://github.com/zahrajamshaid/bigfoot-trailers-releases/releases/latest/download/BigfootTrailers.cer), then:
   - Right-click it → **Install Certificate**
   - **Local Machine** → Next
   - **Place all certificates in the following store** → Browse… → **Trusted People** → OK → Next → Finish
2. **Install the app** by opening this link:
   <https://github.com/zahrajamshaid/bigfoot-trailers-releases/releases/latest/download/BigfootTrailers.appinstaller>
   Windows App Installer opens and installs "Bigfoot Trailers".

From then on the app **checks for updates on every launch** and installs new
versions automatically — no need to come back here.

## Portable version (no install, no admin)

Prefer not to install? Download
[`BigfootTrailers-Portable.zip`](https://github.com/zahrajamshaid/bigfoot-trailers-releases/releases/latest/download/BigfootTrailers-Portable.zip),
unzip it anywhere, and run `bigfoot_mobile.exe`. The portable build does **not**
auto-update — grab a newer ZIP from [Releases](../../releases) when one is published.

## Requirements

- Windows 10 (64-bit) version 1809 or newer, or Windows 11.
- Internet access to `https://bigfoot-trailers.duckdns.org`.

## Troubleshooting

- **"Windows protected your PC" (SmartScreen):** click **More info → Run anyway**.
- **App Installer says the package is untrusted:** the certificate step above
  wasn't completed on this machine.
- **Not updating:** make sure you installed via the `.appinstaller` link (not the
  raw `.msix`); only the App Installer path carries the auto-update setting.

## For maintainers

Releases here are published automatically by the `Windows — Publish Release`
GitHub Action in the private source repo (triggered by pushing a `vX.Y.Z` tag).
Asset names are stable, so `releases/latest/download/<name>` always points at the
newest build — which is what `BigfootTrailers.appinstaller` references.
