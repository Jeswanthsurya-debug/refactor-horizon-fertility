# Horizon

## Problem
Reproductive health changes over time, but a single number can mislead or falsely reassure. Horizon is a solo-built, guest-mode concept for the Future Health Digital Innovation Challenge, **[Fertility] Reproductive Potential**. It helps someone notice observations, understand uncertainty and prepare for earlier conversations. It does not diagnose or estimate pregnancy probability.

## Submission Status
The requested feature flows are implemented, but this is not yet verified as submission-ready. `index.html` is approximately 52.3 KB, above the 45 KB target; its built-in byte-budget check will report that failure when HTTP size is available. A browser runner was not available, so console cleanliness, interactive tests, print pagination and WCAG conformance remain unverified. A nonessential Tailwind CDN asset also remains, so this is not a zero-external-asset build.

## Features
- Navy/teal responsive interface, subtle transform-only motion, reduced-motion and forced-colors support.
- Historical cycle-variation chart with text description and table alternative; separate input-completeness ring.
- Twelve-month timing what-if, five personalized discussion options and per-factor explanations.
- Daily wellbeing log, fourteen-day tracker and gap-aware engagement streak, never used as fertility inputs.
- Local clinician view with a one-page print stylesheet and clearly synthetic population-insight demo.
- Thirty-second, six-step captioned tour with pause/resume and no changes to real data or grants.
- Separate revocable permissions for profile, timeline, logs, local save, clinician display, trusted-person support and on-device AI wording.
- Neutral, user-opened WhatsApp link. No contacts, health details, automatic sending or background alerts.

## How It Works
The first view contains fictional data, kept separate from guest entries. Cycle points show the longest minus shortest of three recent cycles. Three check-ins are required; a two-day first-to-last difference is an illustrative direction rule, not a clinical threshold. Inapplicable cycle fields are excluded. The ring measures weighted input coverage, not fertility or statistical confidence.

Age-context step curves cover ages 18-50 for egg/ovarian and sperm/testicular contexts, not gender identities. They reflect discussion thresholds, not biological decline curves. The internal timing category cannot decrease in the what-if. It is never shown as a fertility index. No future cycle trajectory is drawn. Options include habits, testing, counselling, preservation and referral discussions. Links in the app explain the underlying ASRM/AUA and CDC guidance.

The explainer always has reviewed rule-based wording. If explicitly allowed and already available, a browser-local Prompt API model can choose between fixed reviewed phrases. No raw inputs are sent to it, no cloud AI is called and Horizon initiates no model download.

## Safety And Privacy
Not calibrated, clinically validated or a medical device. A stable trend cannot rule out a problem. It cannot measure ovulation, egg supply, sperm, tubes or embryo quality, and hormonal treatment may make cycle observations inapplicable. Partner factors and other routes to pregnancy need individual clinical context. No proven effect on earlier completed care is claimed; population counts are invented.

No login, backend, analytics, advertising or third-party health-data submission. Never use this app for insurance, employment, credit, screening, ranking or eligibility. All real-data grants start off. Saving is optional and uses one versioned, unencrypted localStorage key, `horizon.private.v2`. Do not opt in on shared devices. Revocation removes the affected saved data; erasure clears the session, drafts, grants, derived output and saved key. Storage failures are reported. Erasure cannot revoke printed copies or a message a user sent outside Horizon.

WhatsApp receives only the fixed neutral message after the user opens the link. The user chooses a recipient and sends it in WhatsApp, under that service's privacy policy. Clinician display, support and AI grants reset after reload. The tour never alters real data or enables permissions.

## Run
Open `index.html` in a current browser, or run `python3 -m http.server 8000` and visit `http://localhost:8000/`. Deploy the file unchanged over HTTPS. No build, installation, backend or API key is required. Core rendering, model and storage are vanilla JavaScript and inline CSS. A nonessential, asynchronous, integrity-pinned Tailwind CDN asset is included; all application features work if it is unavailable. This is the only page-load external asset.

## Verify
Open `/?test=1` or call `runHorizonTests()` in DevTools. The visible panel and console cover both age-context curves, boundary ages, missing-data limits, monotone what-if timing, streak gaps, corrupt storage, input clamping, consent filtering, neutral messaging and isolated erasure. The byte-budget test runs when the browser reports decoded HTTP size; use `wc -c index.html` for the on-disk limit of 45,000 bytes.

Manually test 320px width, 200% zoom, Tab and arrow-key tabs, Escape from dialogs, reduced motion, forced colors and clinician print preview. Log fictional days, enable local save, reload, revoke each grant and erase. Tests use fixtures and injected memory storage; they do not erase guest data. Interactive browser verification still requires a browser runner or a manual pass.

## Deployment Limits
The CSP uses a hash-authorized, fixed bootstrap and an integrity-pinned CDN script, without unsafe script evaluation, inline handlers or network connections. It permits inline stylesheet elements for this single-file design. Keep the bootstrap text and script order unchanged or regenerate its CSP hash. A static host should also send `Content-Security-Policy: frame-ancestors 'none'`; meta CSP cannot enforce framing protection. Browser-local AI availability and file-URL persistence vary by browser. The local-save limit is small and there is no synchronization across devices.

## Changes
- Reworked the interface around observed direction, uncertainty and actionable discussion choices.
- Added consented persistence, daily reflection, trusted-person support, captioned tour and printable summary.
- Centralized schemas, sanitization, model constants, storage handling and batched DOM rendering.
- Expanded accessibility, privacy disclosures, evidence notes and built-in regression checks.