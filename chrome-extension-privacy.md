---
title: Lowtrace browser extension privacy policy
permalink: /chrome-extension/privacy/
---

# Lowtrace privacy policy

_Last updated: 2026-10-13_

Lowtrace is an ad and tracker blocker that runs entirely in your browser. It has no
servers, no accounts and no analytics.

## What the extension collects

**Nothing.** The extension does not collect, transmit, sell or share any personal data or
browsing data, and it keeps no record of the pages you visit. That includes your browsing
history, your search terms, page content, your IP address and usage statistics. The developer
receives no data from the extension. The only site names Lowtrace saves are the ones you
choose to add to your own settings, as described below. If you buy a license key, the
developer does receive what you enter at checkout, such as your email address: see
[Purchases](#purchases).

## What Lowtrace saves in your browser

- **Your settings and rules** are saved with Chrome's `storage.sync` API:
  - your settings (which filter lists and features are on);
  - your allowlist: the host names of sites where you turned blocking off (for example
    `news.example.com`);
  - elements you hid with "Hide an element": the site's host name and a CSS selector;
  - your custom rules.

  If you have turned on Chrome Sync, Google stores these in your Google account and copies
  them to your other signed-in Chrome profiles, under Google's privacy policy. Lowtrace
  never sends them anywhere else. If you allow Lowtrace in Incognito windows, changes you
  make there (for example turning blocking off for a site) are saved to these same settings.
  You can review, remove or export them on the settings page.
- **Your license key**, if you enter one, is saved the same way and synced with your
  settings. It is checked offline, inside the extension, and contains only a random license
  number and an issue date. It holds no name or email address. Exported settings files never
  include it.
- **When your free trial started:** the date and time Lowtrace first ran, which starts
  the 7-day trial. It is saved in `chrome.storage.local` on this device and with
  `storage.sync`, so if Chrome Sync is on, your other signed-in Chrome profiles continue the
  same trial instead of starting a new one. It is used only to tell when the trial ends,
  never sent to the developer, and never included in exported settings files.
- **A status record** is kept in `chrome.storage.local` on this device for the settings
  page and popup: which filter lists are on; whether you are in the free trial, past it, or
  licensed, with the trial's end date or your key's license number; and the last error.
  Next to it, Lowtrace keeps a copy of the enabled filter lists' complex element-hiding
  selectors and the sites they don't apply to, used to hide elements before the background
  responds. That copy holds no personal data and contains your license key only as a hash.
- **Blocked-request counts** come from Chrome itself. They are shown to you and never
  stored or transmitted.
- **Page structure:** to decide which page elements to hide, Lowtrace's content script
  reads the CSS class names and ids on the pages you visit. It hands them to the
  extension's own background script on your device, which adds the matching hiding rules
  (including your own rules that apply to that site) to the page as a stylesheet the
  website can't read. On sites where you turned blocking off, or with element hiding off,
  the content script reads them only until the background answers, then stops. The class
  names and ids are not stored after the page closes and are never transmitted.
- **What a page can see:** in the rare case Chrome doesn't allow that stylesheet for a page,
  Lowtrace uses an ordinary style element instead, which the page can read. It then
  holds only the filter lists' rules, never your own. When a page shows its first frame
  before that stylesheet is in place (the first page after the background was idle, and now
  and then a page that renders very quickly), the enabled filter lists' complex selectors are
  also put in as a style element until the stylesheet arrives: a few milliseconds, or up to
  about 150 ms after a pause. From it a page can tell which filter lists you have on,
  including the Annoyances list, which it could also infer from which elements get
  hidden. It never contains your own rules.

## Network requests

Lowtrace makes no network requests of its own. It blocks requests that match its filter
lists. Filter lists ship inside the extension package and are updated only through normal
Chrome Web Store updates.

## Purchases

Lowtrace is free for 7 days, then needs a license key. If you buy one, the purchase
happens on the payment provider's website, under that provider's privacy policy: the
provider, and through it the developer, receives what you enter at checkout, such as your
email address, to deliver the key. The extension never sees your payment details, and it
never reports which key you entered, whether you are in the trial, or how you use
Lowtrace. The "Buy a license" links in the extension open that website only when you
click them.

## Changes

If this policy changes, the new version will be published at this address with a new
date. Lowtrace will never begin collecting data without a new, clearly disclosed
version of the extension.

## Contact

Questions: <your support email address>
