# Progress Profile: Student Performance Predictor

A single-page website that predicts how a student is likely to score, shows a risk level, and gives warnings with clear next steps. Teachers can add a whole class and see who needs help first.

## Features

- **Prediction:** a score out of 100 and a grade from A to F, worked out from six habits.
- **Warnings:** critical and watch alerts, such as attendance under 75%, too little sleep, or missing assignments.
- **Student profile:** enter name, class, school, ID, target score and an optional photo. The profile shows the prediction, a habit snapshot and the gap to the target.
- **Teacher view:** add many students, see the class average, how many need attention, and a roster sorted from lowest predicted score up.
- **Extra pages:** Home, How it works, and Tips.
- Works on phones and desktops, with light and dark mode.

## How the prediction works

| Input | Weight |
|---|---|
| Previous exam average | 30% |
| Attendance | 20% |
| Assignments submitted | 20% |
| Study hours per week (20 h is full marks) | 15% |
| Sleep (8 h is best) | 8% |
| Phone, games and social media time | 7% |

| Predicted score | Grade | Risk |
|---|---|---|
| 85 and above | A | Low |
| 70 to 84 | B | Low |
| 55 to 69 | C | Moderate |
| 40 to 54 | D | High |
| Below 40 | F | Critical |

The weights are a simple rule of thumb and are not trained on real school data. Results are estimates, not guarantees.

## Run it

No install or build step is needed.

1. Download `index.html`.
2. Open it in any modern browser.

To host it, upload `index.html` to GitHub Pages, Netlify, or any static host.

## Privacy

There is no server or database. Profiles and the class roster are saved in the browser's local storage on the device being used, and are never sent anywhere.

## Limitations

- Data is not shared between devices, so a teacher cannot see students entered on other devices.
- The model is not trained on real data. To make it more accurate, replace the weights in the `analyse()` function with values fitted to your own records.

## Built with

HTML, CSS and vanilla JavaScript in a single file.
