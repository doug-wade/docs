---
title: Snyk Test on your pull requests
---

![Snyk Test on pull requests](http://res.cloudinary.com/snyk/image/upload/q_auto,f_auto,w_auto/v1474294875/Snyk_Test_in_PR.png)

Snyk tests will be visible in pull requests on repos that you are watching with Snyk.
You can review and adjust the settings for this by going to the 'Settings' for the watched project:

![Snyk Test on pull request settings](http://res.cloudinary.com/snyk/image/upload/q_auto,f_auto,w_auto/v1474296632/Snyk_Test_PR_Settings.png)

* By default, Snyk runs a test when the dependencies in the package.json change, and fails the test if the new dependencies have vulnerabilities.
* You can change this to fail if the repository has any existing vulnerabilities (so tests will fail even if the current PR is not adding new vulnerable dependencies).
* You can choose to fail tests only for high severity vulnerabilities.
* You can disable Snyk tests in pull requests.
