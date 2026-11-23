# wa.me QR Generator

A simple, free tool to create WhatsApp QR codes — no WhatsApp Business app, no account, no sign-up.

**Live tool:** https://oswald-creator.github.io/wa-me-qr-generator/

Enter a phone number, optionally add a pre-filled message, and download a QR code that opens a WhatsApp chat with that message already typed. Built as a side project to help members of The Church of Jesus Christ of Latter-day Saints — missionaries, wards and branches — share contact QR codes on posters, programmes and table cards.

## How it works

1. **Number** — pick the country, type the number in any format. Formatting, `+` and leading zeros are cleaned up automatically. Numbers must be in international format (country code + number, digits only in the final link).
2. **Message** — optional pre-filled message, with editable templates (general enquiry, schedule a visit, event details, Sunday services, and more). Add an optional placement tag like `[foyer-poster]` to tell apart where a scan came from, and an optional label for the printed sign.
3. **Download** — live QR preview, the exact `wa.me` link, and a decoded "what the scanner will see" proof. Download the QR as PNG (512 / 1024 / 2048 px) or SVG, copy the link, test it, or download a printable sign with your label above the code.

Everything runs entirely in the browser. No phone number or message is uploaded, stored, or tracked.

## The link format

```
https://wa.me/<country-code-and-number>?text=<url-encoded-message>
```

Example: `https://wa.me/15551234567?text=Hello%2C%20I%27d%20like%20to%20learn%20more`

## Guide

A step-by-step PDF covering WhatsApp Business QR codes, hand-built `wa.me` links, templates, printing tips and troubleshooting is in [`docs/whatsapp-business-qr-how-to-guide.pdf`](docs/whatsapp-business-qr-how-to-guide.pdf).

> **Never share a WhatsApp linked-device pairing QR code** (the one under WhatsApp > Settings > Linked Devices). That is a private login code, not a contact code. The QR codes this tool makes are safe to print and share.

## Tech

A single static `index.html` — no build step, no backend, no dependencies except the [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) library loaded from cdnjs. Hosted free on GitHub Pages; every push to `main` redeploys automatically.

## Licence

MIT-0 (MIT No Attribution) — see `LICENSE`. Use, copy and modify it freely; no attribution or credit is required.
