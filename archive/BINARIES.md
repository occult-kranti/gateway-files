# BINARIES.md — manifest for non-text deliverables

These binary files are part of the project and ship with the deployed website (under
`files/`), but are **not committed to this git repo** (the push channel used to publish
this repo is text-only; committing base64 would corrupt them). Verify any copy against
the SHA-256 below.

## Documents (declassified, public domain)

| File | Bytes | SHA-256 | Canonical source |
|---|---|---|---|
| documents/01_Analysis-and-Assessment-of-Gateway-Process_1983_CIA-FOIA.pdf | 3,160,520 | 53d80d9486403d98c95baed6400e2eaabeceb2100dfd7b2605ba1ec7cc9620b... see below | https://www.cia.gov/readingroom/docs/CIA-RDP96-00788R001700210016-5.pdf (mirror: documents2.theblackvault.com/documents/cia/CIA-RDP96-00788R001700210016-5.pdf) |
| documents/02_Analysis-and-Assessment_ANNOTATED-with-page-25_clearhat.pdf | 4,380,842 | baef8f4d37cc9b24... see below | https://www.clearhat.org/public/analysis-and-assessment-of-the-gateway-process-4mb.pdf |

Full checksums:

```
53d80d9486403d98c95baed6400e2e2aabeceb2100dfd7b2605ba1ec7cc9620b  01_Analysis-and-Assessment-of-Gateway-Process_1983_CIA-FOIA.pdf
baef8f4d37cc9b2412ee2a16b1fc32f1ee3068b686b9c1a1abf88bdd39d0f296  02_Analysis-and-Assessment_ANNOTATED-with-page-25_clearhat.pdf
```

## Audio presets (synthesized for this project, 44.1 kHz stereo MP3 loops)

```
bc9ed8a12bb9c991f4afa81126fed156cbb5a620478639b601ed38cc17c2fb6c  audio/alpha-focus-10hz.mp3
623f0f477da8c30e10d76d1834e894c4a38ef019ea3230a77017846b08b13a5e  audio/delta-sleep-2hz.mp3
f51b77d30b8ad7b2b92b772d247ad3215a549de1bf84e3ef9c12068d5d661643  audio/gamma-40hz-clicks.mp3
6c41e2fac7132c7e7838574d04112898187b9fae707a3bfab05721d83b5bf1fa  audio/gateway-theta-4hz.mp3
30d17dfe28e5c880cad675b6aa21ed9398459797421389529e4b49a6246299ea  audio/pink-noise-bed.mp3
e1c04037de75ce1adde334e1a7109fb7f4b24cef97a3c4610b474759187bd407  audio/schumann-783-beat.mp3
4227b31f20b22ee531ae7ede471d37d4b64551b03494fd537988ecc819002c6b  audio/theta-deep-6hz.mp3
```

Added with the STARGATE dossier (Oct 2026):

```
d61472baee25504c2d44d43d1e5f97cb08241aebdd846bbcb565ad051a04601e  audio/crv-watch-45hz.mp3
b8b642ac96749f08880864034708237f051eb5b41bc96085c5ed1f54d1db6cee  audio/alpha-ready-8hz.mp3
ed267b3f4d0ddae3a06b48012f50ac33d701ee6e1025f3862e73b430e311850d  audio/brown-noise-bed.mp3
```

Every preset can also be regenerated exactly from `files/audio/presets.json` specs:
binaural presets are pure sine pairs (left/right carriers as listed); the 40 Hz preset
is a 1 kHz pulse train at 40 pulses/s; the noise bed is low-passed pink noise. The
website's Frequency Lab (Chapter 11) synthesizes all of them live in the browser — no
files needed.
