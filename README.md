# MobileVeinViewer — Thesis

**Vein Viewing System Using Hardware Extension Attached To Smartphones**

Master's Thesis in Informatics  
Technische Universität München, Department of Informatics  
Author: Bakri Bitar &nbsp;|&nbsp; Supervisor: Prof. Dr. Uwe Baumgarten  
Submission Date: November 15, 2018

📱 **[View the Android application repository](https://github.com/bakribitar/MobileVeinViewer)**

---

## Abstract

The goal of this thesis is to develop a low-cost non-invasive vein viewing system on Android smartphones that helps healthcare workers identify the superficial veins, locate and examine them by providing an accurate AR image in a real-time manner.

Venepuncture and starting an intravenous cannulation are frequently required skills in healthcare facilities for investigative or diagnostic purposes. Finding the right vein is a substantial prerequisite for such operations and could be time consuming — moreover, it is unfortunately not risk free, as numerous associated complications have been described, including misplaced puncturing or even accidental arterial puncturing and cannulation, causing a life threat or unnecessary pain and stress to the patient in best cases. Dedicated devices for viewing and locating veins have been launched in the market; although they seem to give excellent results in terms of accuracy and performance, they include advanced and expensive hardware which makes them unaffordable for some countries or clinics.

The proposed solution includes a low-cost hardware extension attached to a smartphone and an Android application that receives and processes data sent from sensors placed on the hardware extension. On the smartphone's screen, healthcare workers should be able to see a real-time video showing the superficial veins with good contrast, and depending on that they can locate the veins and puncture them with much less probability of misplaced puncturing.

NIR (Near-Infrared) light at a wavelength of 940 nm via LEDs, together with a digital video camera sensitive only to the infrared spectrum (obtained by replacing the light filters in a normal webcam), were used. Because of NIR light-absorption properties of the oxygenated blood carried by the veins, it was possible to increase the peripheral veins' contrast and, using image processing algorithms, visually isolate them on the received video in real time.

---

## Thesis Contents

| Chapter | Topic |
|---------|-------|
| 1 | Introduction — venepuncture complications, infrared radiation background, prior work |
| 2 | Skin- and Blood-Light Interaction — wavelength selection rationale |
| 3 | Hardware Extension — OTG cable, NIR LEDs, NIR camera, power consumption, safety |
| 4 | Software Application — methodology, image processing modes, application architecture |
| 5 | Results and Discussion — results on tattooed skin, different skin colours, skin diseases |
| A | Appendix: Compatible Android Devices |
| B | Appendix: Incompatible Android Devices |
| C | Appendix: Verified Web Cameras |

---

## Reading the Thesis

The compiled thesis PDF is available at [`build/main.pdf`](build/main.pdf).

---

## Building the PDF

### Dependencies

```bash
sudo apt-get install texlive-latex-base biber inotify-tools
```

### Quick Start

1. Clone this repository
2. Enable automatic compilation (re-compiles whenever a `.tex` file is saved):

```bash
./helputils.sh 2
```

3. When you update the bibliography (`.bib` file), run a full bibliography build:

```bash
./helputils.sh 5
```

### All `helputils.sh` Commands

| Command | Description |
|---------|-------------|
| `./helputils.sh 1` | List all available options |
| `./helputils.sh 2` | **Automatic compilation** — watches for `.tex` file changes and recompiles |
| `./helputils.sh 3` | Delete build artifacts (log files, etc.) without removing the PDF |
| `./helputils.sh 4` | Remove trailing whitespaces from `.tex`, `.sh`, and `.bib` files |
| `./helputils.sh 5` | **Full bibliography update** — required after changes to the `.bib` file |

> **Tip:** Before committing to Git, run `./helputils.sh 3 4` to clean build files and strip trailing whitespace.

---

## Repository Structure

```
build/          # Compiled PDF output
logos/          # TUM and faculty logos
chapters/       # Individual thesis chapter .tex files
figures/        # Figures and images used in the thesis
bibliography.bib
main.tex        # Root LaTeX document
helputils.sh    # Build helper script
```

---

## Template

This thesis was written using the [TUM Informatics LaTeX Thesis Template](https://github.com/fwalch/tum-thesis-latex) by Florian Walch and contributors. The forked template introduces the following modifications over the original:

- Replaced the `Makefile` with `helputils.sh` — a bash script with additional functionality (automatic compilation, artifact cleanup, whitespace removal, bibliography update)
- University and faculty logos bundled directly in the `logos/` directory (original template pointed to invalid URLs)
- Logo-cropping script removed (logos are already the correct shape)
- Added an **Abbreviations and Acronyms** page

---

## License

### Thesis Content

Copyright © 2018 Bakri Bitar. All rights reserved.

### LaTeX Template

[![Creative Commons License](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

The LaTeX template is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/), meaning:

- You can share (copy, redistribute) and adapt (remix, transform, build upon) this template for any purpose, even commercially.
- If you share the template or a derived version, you must attribute the original authors Florian Walch and contributors by providing a link to the [original template](https://github.com/fwalch/tum-thesis-latex) and indicate if changes were made.
- Any derived template must use the same or a compatible license.

The license applies only to the template; there are no restrictions on the resulting PDF file or the contents of the thesis.
