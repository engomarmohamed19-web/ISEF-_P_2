# MedBand

**Smart Bracelet — Health in Your Hand** is a student research prototype concept exploring wearable sensing, medical-profile access and emergency-alert ideas. This folder is a complete, dependency-free static website source project.

> MedBand is not a certified medical device or diagnostic tool, and does not replace professional medical care. This demo has no connected hardware. Values such as 78 BPM and SpO₂ 97% are fictional illustrative data.

## Requirements

- A modern browser (current Chrome, Edge, Firefox or Safari)
- Optional: Python 3 or Node.js if you want to serve the files over localhost

There are no paid services, API keys, build dependencies or third-party runtime libraries.

## Run locally

The simplest option is to open `index.html` in a browser. For a local HTTP server, run one of these commands from this folder:

```bash
python -m http.server 8000
```

or:

```bash
npx serve .
```

Then open `http://localhost:8000` (Python) or the local URL printed by `serve`.

## Production build

This is a static site, so the production build is the project folder itself. Copy the folder to any static web host. Before publishing, review the medical safety language, project status and privacy guidance against the actual prototype and school requirements. No package installation or compilation is needed.

## Project structure

```text
medband-website/
├── index.html       Semantic, responsive single-page site
├── styles.css       Design system, responsive layouts, RTL and reduced-motion rules
├── app.js           English/Arabic strings and all interactions
├── assets/
│   └── favicon.svg  Local MedBand mark
└── README.md
```

## Language and accessibility

The header language button switches the complete user interface between English and Arabic, updates the document language and text direction, and remembers the choice in local storage. Chart diagrams and the bracelet remain oriented appropriately in RTL. The site supports keyboard navigation, visible focus from native controls, dialog dismissal, reduced-motion preferences and mobile navigation.

## Images and concept visuals

Artwork is built from local CSS illustrations and a local SVG favicon; the site does not depend on remote image URLs. To replace the bracelet or gallery concepts, edit the related markup in `index.html` and the rules in `styles.css`. Keep demo values clearly marked and do not imply certification or clinical performance.

## Interactions

- Responsive navigation and persistent EN / عربي language switch
- Searchable and filterable component catalogue with detail dialogs
- Pointer and keyboard rotation for the interactive 2.5D bracelet concept
- Five app-preview tabs with fictional profile, chart, history, emergency and settings screens
- NFC profile-access concept, with explicit privacy guidance
- Timed illustrative alert-flow simulation and reset control
- Selectable gallery illustrations with a keyboard-dismissable viewer
- FAQ and research-limitations disclosure panels

## Future hardware integration

No live hardware connection is implemented. A future integration should first document the exact board revisions and sensor breakouts, power and battery-protection design, pin mapping and sampling settings. Then:

1. Validate each sensor against suitable reference equipment under controlled conditions. Document fit, motion, signal quality and known error sources.
2. Design a documented BLE data format and connection-state/error handling. Keep local and demo data separate from measured data.
3. Add an app data layer that clearly distinguishes measurements, stale data and unavailable hardware. Do not transmit health data to third parties without a valid need, consent and security review.
4. Store only a non-sensitive identifier or protected link on NFC tags. Enforce access controls on the destination; avoid putting medical records in tag memory.
5. Evaluate alert thresholds, false alarms, latency, acknowledgement usability and safe operation before any real-world use. Motion alone cannot prove a fall or fainting event, and readings do not diagnose disease.
6. Review electrical, battery, privacy, consent, school research and applicable regulatory requirements with qualified supervisors. Do not represent a student prototype as a clinical or emergency-response product.

## Background references

The site's links point to manufacturer or technical background pages for the ESP32-C3, MAX30102 and NFC. They are references for further study, not evidence that this assembled concept is compatible, validated or clinically accurate.
