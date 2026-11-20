# refactor-horizon-fertility
# Horizon: Reproductive Potential Trend Companion

**Future Health Digital Innovation Challenge** · Challenge: **[Fertility] Reproductive Potential**
Solo entry by **J. Jeswanth Surya** (Dr. M.G.R. Educational and Research Institute, Chennai, India)

**Live demo:** https://jeswanthsurya-debug.github.io/refactor-horizon-fertility/

Horizon shows the **direction of change** in reproductive potential over time. It does not give a fertility score or a diagnosis. It explains the picture in plain language, suggests next steps, and gives clinicians a one-page summary, while the user stays in control of their data.

## The problem
Most people only get a real assessment when they are already trying to conceive or struggling. The relevant information is scattered across history, lifestyle, conditions and lab results, so people over- or under-estimate their risk, and clinicians have no simple way to see who could benefit from earlier counselling.

## How Horizon answers the challenge
| Challenge need | What Horizon does |
|---|---|
| Longitudinal view | Trend chart, 12-month what-if, daily check-in log |
| Plain-language interpretation | Changeable vs not-changeable factors, confidence meter, simple explainer |
| Timely, personalised options | Healthy habits, testing, counselling, fertility-preservation talk, referral |
| Clinician and system usefulness | One-page clinician summary and a population insight panel (synthetic data) |
| Privacy, non-discrimination, control | Separate consent per data type, opt-in local saving, one-tap erase, never used for insurance, employment, credit or ads |
| Evidence of earlier action | Success measures in the deck; calibration and false-reassurance limits stated in the app |

## Features
- Guest mode: no login, no account, works immediately
- Per-category consent that can be switched off at any time
- Trend view with a data-completeness meter, so missing data lowers confidence instead of giving false certainty
- 12-month what-if that changes only the factors a person can actually change
- Daily check-in log with streak
- Optional trusted person: a pre-written WhatsApp message that contains **no health details** and is only sent when the user presses send
- Clinician view with every factor and its weight
- Dark, minimal interface with gentle motion; respects reduced-motion settings; keyboard accessible

## How it works
1. A sex-specific age curve gives a baseline.
2. Transparent factor weights adjust it (weight range, sleep, smoking, known condition, family history, optional lab result, pattern variability).
3. Completeness of the data sets how confident the result looks.
4. The what-if removes only the changeable penalties.

The weights are visible in the code. They are education-level heuristics, not a validated clinical model.

## Run it
Open `index.html` in any modern browser. No install, no build step, no server, no dependencies.

## Safety and privacy
- Runs entirely in the browser; no analytics and no third-party scripts
- Saving is opt-in and stays on the device; "Erase all my data" removes it
- User text is inserted as text, never as HTML
- Not a medical device and not a diagnosis. If you are worried, please speak to a qualified clinician

## Limits and next steps
The prototype weights need calibration against clinician-labelled cases. The population panel uses synthetic data only. Roadmap: clinician calibration study, Arabic, Hindi and Tamil interface, clinician dashboard, FHIR connector.

## Author
J. Jeswanth Surya · GitHub: [@Jeswanthsurya-debug](https://github.com/Jeswanthsurya-debug)
