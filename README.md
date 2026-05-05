# Drivetrain Calculator

A live, browser-based drivetrain calculator for robotics. Configure a multi-stage gearbox, set a wheel/tread diameter, and solve for linear speed in real time.

**Live:** https://adamkdean.github.io/drivetrain-calculator/

## What it does

- **Gearbox / Gear Train** — chain together simple and compound gear stages, set the motor input RPM, and read out total reduction, mechanical advantage, output RPM, and stage count. Math: `ω_out = ω_motor ÷ ∏(N_driven ÷ N_driver)`.
- **Wheel / Tread** — set wheel diameter, wheel rotational speed (ω), and linear speed (v). Lock any two; the third is solved live from `v = π · D · ω`. Diameter accepts mm / cm / m / in; speed reports in mm/s, cm/s, m/s, km/h, mph.
- **Link gearbox → wheel** — toggle the link icon to drive wheel ω directly from the gearbox output, so a change anywhere upstream propagates straight through to linear speed.
- **Extras** — circumference, time per revolution, RPS, and speed in multiple units update on every change.

## Use

Just open https://adamkdean.github.io/drivetrain-calculator/ — no build, no install, no backend. Enter motor RPM, edit gear teeth counts, set the wheel diameter, and the rest solves itself.

## Run locally

It's a single self-contained HTML file. Clone and open `index.html` in a browser:

```sh
git clone git@github.com:adamkdean/drivetrain-calculator.git
cd drivetrain-calculator
open index.html
```

## Stack

Plain HTML + CSS + vanilla JS. Font Awesome via CDN. No framework, no build step.
