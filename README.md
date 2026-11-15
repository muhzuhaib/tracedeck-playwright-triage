# Tracedeck - Playwright Triage

Support, documentation and legal documents for the **Tracedeck** plugin for JetBrains IDEs.

**[Get it on the JetBrains Marketplace](https://plugins.jetbrains.com/search?search=Tracedeck)**

**This repository holds no source code.** It gives the plugin a real issue tracker and real documentation, both
linked from the Marketplace listing.

- **Report a bug or ask for a feature:** [open an issue](../../issues), or email
  [support.zuhaib@gmail.com](mailto:support.zuhaib@gmail.com). Every message gets a reply.

---

## What the plugin does

Tracedeck opens Playwright traces and the test results you download from CI inside your IDE. It groups every failure
by its cause, gives each one a Failure Card, and jumps from any recorded action to its line in your test.

### Free, with no time limit

- **Open a trace with a double-click.** A `trace.zip` opens in an editor tab, shown with your project's own Playwright
  Trace Viewer, or with the viewer that comes with Tracedeck when the project has none.
- **From an action to its test line**, for JavaScript, TypeScript, Python, Java and .NET tests. Paths recorded on a
  Linux or Windows CI runner are matched to the files in your project.
- **Open the test results you downloaded from CI:** the zip of your CI run, holding the HTML report, JSON results,
  sharded blob reports or a plain `test-results` folder (a zip inside a zip works too). Download the artifact from your CI first; Tracedeck does not
  connect to your CI.
- **Every failure grouped by its cause**, with a count, the tests in the group and when it first and last happened.
- **A Failure Card for each failure:** the error, the failing action and its test line, the action before it, the
  locator's Playwright log, console and page errors, and failed requests.
- **Tests that passed only on retry**, listed on their own.
- **A one-line check of your trace setting**, saying what it lets Tracedeck compare, with a "Copy setting" button.
- **A Triage Report** for your pull request: one Markdown file, with passwords, tokens and other values masked.

- **Compare with a passing trace** on a Failure Card: lines the failing trace up with a passing one, action by
  action, stops at the first action where the runs went differently, with its test line, and shows the failing action
  side by side, the requests and console messages that differ (common noise greyed out) and the time per action. The
  passing side is a passing retry in the same artifact, an older green CI artifact, or any passing `trace.zip` you
  choose. The result joins the Triage Report.

### Paid: Why it fails on CI

For the test that fails on CI and passes on your machine. One click on a Failure Card or a group:

- re-runs the test locally several times with tracing on and says how often it fails ("reproduces 2 of 5");
- shows what the page did differently (the elements around the locator at the first difference, and how many
  elements the locator matched on each side) and what the machine did differently (browser and Playwright version,
  operating system, viewport, locale, timezone, base URL);
- for a group, names the differences all its tests share;
- adds all of this to the Triage Report.

## Getting started

1. Install Tracedeck from **Settings | Plugins | Marketplace**.
2. Double-click a `trace.zip` in the Project view, or use **File | Open Playwright Trace or Artifact...** and pick the zip your CI run saved (or a `playwright-report` folder, to see the report itself).
3. For a CI run, the failures appear grouped. Click a group to see its Failure Cards, and click any action to open its
   test line.
4. To try the paid features, click **Why it fails on CI (paid)** on a Failure Card, then **Get licence** to start
   the free 30-day trial through JetBrains.

## Requirements and known limits

- IntelliJ IDEA, WebStorm, PyCharm or Rider, version 2026.1 or 2026.2.
- Traces from Playwright 1.62 to 1.64. A trace from another version opens with a banner saying so.
- The paid local re-run uses the Node, Playwright and browsers (or Python and pytest-playwright) your project already
  has. If one is missing, Tracedeck says which in place and installs nothing.
- A local re-run is labelled "Local environment": your machine cannot match every detail of CI (operating system,
  CPU load, fonts). Comparing with a passing retry or an older green CI artifact compares CI with CI.
- Tracedeck version 1 does not support remote development.

## Pricing

- **Personal:** $2.40 per month, or $24 per year.
- **Commercial:** $5.90 per month, or $59 per year.
- Every free feature above is **free**, with no licence and no trial clock. The prices are for **Why it fails
  on CI**, which starts with a **free 30-day trial** from the **Get licence** link, or from **Help | Register**.

## Privacy

Tracedeck sends nothing to the vendor. It has no telemetry, no analytics and no account. It makes no network calls
except to a local address on your own machine, where it shows the trace viewer. The full policy is in
[PRIVACY.md](PRIVACY.md).

## Support

Open an issue here or email [support.zuhaib@gmail.com](mailto:support.zuhaib@gmail.com). Include the IDE and version
(**Help | About**), the plugin version, and what you clicked. **Traces can hold passwords, tokens, cookies and internal
addresses: please share a Triage Report, which is masked, and check anything before you attach it.**

## Legal

- [End User Licence Agreement](EULA.md)
- [Privacy Policy](PRIVACY.md)
- [Third-party notices](THIRD-PARTY.md)

The plugin itself is not open source. This repository is for support and documentation only.
