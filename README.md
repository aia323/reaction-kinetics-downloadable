# Reaction Kinetics: Downloadable App

An interactive app for exploring sequential chemical reactions (A → B → C).
Students move sliders for rate constants and reaction orders, and the
concentration plots update live. A Play button animates how A, B and C change
over time. The goal is to find the settings that give the most B.

The original app was built by a previous student group for Lehigh University's
Chemical and Biomolecular Engineering teaching modules. In Summer 2025, I turned it
into a downloadable version so students can run it on their own computer without
a server.

## My role
- **Packaged the app as a standalone Windows program** (`.exe`) using PyInstaller.
- **Set up automatic builds with GitHub Actions**: every push builds a fresh
  Windows executable (`.github/workflows/build-windows.yml`).
- Set up the project's dependencies (`requirements.txt`) for a clean install.

## How it works
The app solves the rate equations for A → B → C with SciPy (`odeint`) and
draws the results with Bokeh.

## Tech
Python · Bokeh · SciPy · NumPy · PyInstaller · GitHub Actions

## Run it locally
```bash
pip install -r requirements.txt
bokeh serve --show ReactionKinetics.py
```
