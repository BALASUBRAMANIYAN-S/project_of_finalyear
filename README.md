# Smart Container Dashboard (Final Year Project)

A single-page web dashboard that shows live load data from an IoT weighing setup, together with a live data sheet and the device's GPS location.

## Features

- **Live weight** reading in grams
- **Underload** and **Overload** status shown as YES / NO (green / red)
- Values refresh automatically every 5 seconds
- **Live data sheet**: an embedded Google Sheet (PDS system), refreshed every 15 seconds
- **GPS location** shown on an embedded Google Map
- Dark mode toggle
- Responsive layout for phones

## How it works

The dashboard reads values from a [Blynk](https://blynk.io/) cloud device through its HTTP API:

| Virtual pin | Meaning |
|---|---|
| `V1` | Weight (g) |
| `V3` | Underload flag (1 = yes) |
| `V5` | Overload flag (1 = yes) |

The hardware side (sensor and microcontroller sending data to Blynk) is not part of this repository.

## Tech Stack

- HTML, CSS and vanilla JavaScript (a single `index.html`)
- Blynk Cloud HTTP API
- Google Sheets and Google Maps embeds

## Getting Started

1. Clone the repo:
   ```bash
   git clone https://github.com/BALASUBRAMANIYAN-S/project_of_finalyear.git
   cd project_of_finalyear
   ```
2. In `index.html`, set the `token` constant to your own Blynk device auth token, and change the Google Sheet and map links if needed.
3. Open `index.html` in a browser.

> Security tip: a Blynk token in a public page lets anyone read (and possibly write) your device data. Keep the token out of the public repo, and regenerate it in the Blynk console if it was ever published.

## Project Structure

```
index.html   # Page, styles and script
```
