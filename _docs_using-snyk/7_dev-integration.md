---
title: Integrating Snyk into your dev workflow
---

<p>To continuously avoid known vulnerabilities in your dependencies, integrate Snyk into your continuous integration (a.k.a. build) system. Here are the steps required to to so:</p>

1. Install the Snyk utility using `npm install -g snyk`.
2. Run `snyk wizard` in the directory of your project following the prompts which will also generate a `.snyk` policy file.
3. Ensure the `.snyk` file you generated was added to your source control (`git add .snyk`).
4. If you selected to, Snyk will include `snyk test` as part of your `npm test` command, so if there are new vulnerabilities in the future, your CI will fail, protecting you from introducing vulnerabilities to production.

If you monitor a project with Snyk, you'll get notified if you're affected by any new vulnerabilities. To make sure Snyk is monitoring the latest status of your project, add `snyk monitor` to your continuous deployment process. You'll need to include your API key as an environment value. Find your API key on the dashboard after logging in.
