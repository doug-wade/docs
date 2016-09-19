---
title: Integration features
---

For each watched repo, you:

* will see Snyk tests in your pull request that check for vulnerabilities
* get email alerts and a Snyk pull request with fixes when new vulnerabilities that affect your repo are disclosed
* get email alerts and a Snyk pull request if a new upgrade or patch is available for a vulnerability that affects you
* can trigger a Snyk pull request with fixes yourself from the test report page or the project page for your repo on snyk.io

**Snyk Test on your pull requests**

![Snyk Test on pull requests](http://res.cloudinary.com/snyk/image/upload/c_scale,w_600/v1474294875/Snyk_Test_in_PR.png)

Snyk tests will be visible in pull requests on repos that you are watching with Snyk.
You can review and adjust the settings for this by going to the 'Settings' for the watched project:

![Snyk Test on pull request settings](http://res.cloudinary.com/snyk/image/upload/v1474296632/Snyk_Test_PR_Settings.png)

* By default, Snyk runs a test when the dependencies in the package.json change, and fails the test if the new dependencies have vulnerabilities. 
* You can change this to fail if the repository has any existing vulnerabilities (so tests will fail even if the current PR is not adding new vulnerable dependencies). 
* You can choose to fail tests only for high severity vulnerabilities. 
* You can disable Snyk tests in pull requests.


**Fix vulnerabilities with Snyk pull requests**

When viewing a Snyk test report for a repo that you own, or when looking at a project that you are watching with Snyk, you’ll see a link to ‘Open a fix PR’:

![Fix button](http://res.cloudinary.com/snyk/image/upload/c_scale,w_644/v1474296125/Open_Fix_PR.png)

This allows you to generate a Snyk pull request with the minimal changes needed to fix the vulnerabilities affecting the repo.You can review the changes, and decide to open a pull request on the 'Open a fix PR' page:

![Open a fix PR page](http://res.cloudinary.com/snyk/image/upload/v1474296317/Fix_PR_page.png)

Here’s an example for the pull request.

![Snyk remediation PR](https://res.cloudinary.com/snyk/image/upload/f_auto,q_auto,w_auto/v1466629389/docs-alert_scaled.jpg)

**Get a Snyk pull request when newly disclosed vulnerabilities affect you**

Whenever a vulnerability is disclosed that affects a repo you’re watching, Snyk will not only email you about it, but also generate a Snyk pull request that addresses the vulnerabilities. It’s the same pull request as in the example above.

**Get a Snyk pull request when new upgrades or patches are available**

When no upgrade is available, you can ignore or patch a vulnerability. When a better remediation option has become available, for example an upgrade for a vulnerability you previously ignored, Snyk notifies you about this via email, and also generates a pull request with the new fix. 

