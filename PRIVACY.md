# Privacy Policy

**Tracedeck - Playwright Triage**
Version 1.0, 15 November 2026
Vendor: **Muhammad Zuhaib Zahid**

## The short version

**The plugin collects nothing.** It has no telemetry, no analytics and no crash reporting, and it sends nothing to the
Vendor. Your traces, your test results and your source code stay on your machine.

## What that means in detail

- **Traces and test results.** Tracedeck reads the traces, reports and CI artifacts you open, in the IDE's process.
  It reads your `playwright.config` file as text and never runs it.
- **The trace viewer.** To show a trace, Tracedeck serves it to the IDE from a local address on your own machine
  (127.0.0.1), behind a path that changes every session. Nothing outside your machine can reach it.
- **Masking.** Passwords, tokens, cookies and other values are masked in Tracedeck's own panels by default, and always
  masked in the Triage Report before it is written.
- **The Triage Report.** It is written where you choose, outside your repository by default (beside the artifact, or
  as a scratch file). Nothing is uploaded.
- **Local re-runs (paid).** Why it fails on CI runs your own test with your project's own Playwright on your
  machine. Any network call your test makes is made by your test, as it would be in any test run. Tracedeck installs
  and downloads nothing.
- **Network.** Tracedeck itself makes no network requests except to that local address.
- **No usage tracking.** The plugin does not record which features you use or anything about your projects.
- **No accounts.** The plugin asks you for no personal information and has no sign-in of its own.

## What the Vendor does receive

Only what you choose to send:

- **A purchase.** JetBrains sells Tracedeck as merchant of record and shares with the Vendor the sales information
  needed to be paid and to comply with tax law. What JetBrains collects at purchase is covered by the
  [JetBrains Privacy Policy](https://www.jetbrains.com/legal/docs/privacy/privacy.html).
- **Support you initiate.** If you email the Vendor or open an issue, the Vendor receives what you write, including
  any trace or report you attach. **Traces can hold passwords, tokens, cookies and internal addresses. Please send a
  Triage Report, which is masked, and check anything before you attach it.**

## Licence validation

Checking that a licence or trial is valid is performed by **the JetBrains IDE**, using JetBrains'
own licensing service, and only when you use a paid feature. That exchange is governed by JetBrains' terms and privacy
policy.

## Changes

If this policy ever changes, the revised version will be published at this address with a new date at the top.

## Contact

Questions about this policy: Muhammad Zuhaib Zahid, at
[support.zuhaib@gmail.com](mailto:support.zuhaib@gmail.com), or by opening an issue on the public issue tracker
linked from the Marketplace listing.
