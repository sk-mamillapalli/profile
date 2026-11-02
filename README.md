# Profile page

Personal profile page, served via GitHub Pages.

This repository contains **only** `index.html` — a single self-contained file with no
build step and no dependencies.

## Source of truth

The master record lives in a **separate private repository**
(`skrishnajimamill/profile`) and contains the résumé sources, supporting evidence,
and notes that must not be published. Edit the page there, then copy `index.html`
here.

```sh
cp ~/Documents/profile/index.html ~/Documents/profile-public/
```

## Deploying

Settings → Pages → Branch `main` → `/ (root)`.

## Before every commit

Confirm nothing sensitive has crept in:

```sh
grep -icE 'rdar|DSID|[0-9]{10}|acc-kcs|docker\.apple\.com' index.html   # expect 0
```
