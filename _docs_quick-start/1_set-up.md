---
title: Set up
draft: true
---

First off, you’ll need a project to test. If you don’t have one handy, you can use our demo application, [snyk-demo-app](https://github.com/Snyk/snyk-demo-app). Simply run these lines to clone it and install its dependencies:

```bash
git clone https://github.com/Snyk/snyk-demo-app.git
cd snyk-demo-app
npm install
```

Now that you have a project to test, you need to install Snyk from npm, change directory to your project’s folder and run Snyk’s wizard. We’ll install Snyk as a global tool for now; later we’ll touch on using it as a local dependency of your automated tests. Run the following in your project’s folder:

```bash
npm install –g snyk
snyk wizard
```

The wizard walks you through finding and fixing the issues found through upgrades and patches, and creates a Snyk policy (a .snyk file) with your decisions. The wizard leverages four other Snyk commands –`auth`, `test`, `protect` and `monitor` – which we’ll explain as we advance.
