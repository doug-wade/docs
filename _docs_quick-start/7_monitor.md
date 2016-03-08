---
title: Monitor
---

Now that you’re free of known vulnerabilities, there are two ways that can change. The first is adding vulnerable packages to your code, which we handle by adding `snyk test` to your test/CI system. The second is through newly disclosed vulnerabilities. These are new disclosures of vulnerabilities in old code – the code you’re running in production!

This is addressed by Snyk’s last step – monitor. The snapshot the wizard takes is saved on Snyk’s servers, remembering the dependencies used on this application. If a newly disclosed vulnerability affects your application, you’ll get an email alerting you to it. You can then run the wizard again to upgrade or patch as needed, and deploy the secure code.

To keep Snyk’s understanding of your application up to date, you can run `snyk monitor` at the end of your deployment process. Doing so will take a fresh snapshot of your application, just like the wizard does, and will ensure Snyk’s alerts apply to your most recent code.

You know have an overview of Snyk test, protect, and monitor, and you’ve used the wizard that walks you through fixing your vulnerabilities. If you’d like to know more, take a look at our detailed documentation, and our FAQ.
