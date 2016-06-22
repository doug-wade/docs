---
title: Integration features
---

For each integrated repo, you: 
* will see Snyk tests in your pull request if new dependencies are added (i.e. when the package.json is modified)
* get email alerts and a Snyk pull request with fixes when new vulnerabilities that affect your repo are disclosed
* can trigger a Snyk pull request with fixes yourself from the test report page or the project page for your repo on snyk.io

**Snyk tests in your pull requests**

Snyk tests will be visible in pull requests on repos that you have added to Snyk. If the dependencies in the package.json change, Snyk runs a test and you can see if it passed or failed in the PR. 

You can set if it should fail for all vulnerabilities, or only for a certain severity level:
* go to the repo's .snyk file
* add `failThreshold: high` if you want only high severity vulnerabilities to cause tests to fail. 
* `failThreshold: medium` will fail test when both medium and high severity vulnerabilities are found. 
* It should look like here in this example.

**Fix vulnerabilities with Snyk pull requests**

When viewing a Snyk test report for a repo that you own, or when looking at a project that you are monitoring with Snyk, you’ll see a button to ‘Fix vulnerabilities’. 

This button allows you to generate a Snyk pull request with the minimal changes needed to fix the vulnerabilities affecting the repo. Here’s an example. 

**Get a Snyk pull request when newly disclosed vulnerabilities affect you**

Whenever a vulnerability is disclosed that affects a repo you’re monitoring, Snyk will not only email you about it, but also generate a Snyk pull request that addresses the vulnerabilities. It’s the same pull request as in the example above.
