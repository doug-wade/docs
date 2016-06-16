
Snyk helps you fix vulnerabilities in your npm dependencies quickly and easily, as well as keeping you vulnerability free on an ongoing basis. Snyk is free for open source, and its testing is free for all - so you can start securing your Node.js and npm applications with just a couple of clicks.

76% of Snyk users found vulnerabilities in their applications, and new vulnerabilities are disclosed regularly, putting your application at risk.

Snyk works in 4 key steps:
- Find vulnerabilities
- Fix vulnerabilities
- Prevent addition of new vulnerable packages
- Respond to newly disclosed vulnerabilities.

All of these can be done using the deep GitHub integration, and on the command line with the [Snyk CLI](https://snyk.io/docs/).

## Find vulnerabilities in your repos
Quickly and easily check all your npm repositories on Snyk’s [test page](https://snyk.io/test/). Snyk will identify the repositories that use npm, calculate their dependencies, and match them up with Snyk's [vulnerability database](https://snyk.io/vuln/).

TODO: Image of add repos page

Vulnerabilities are classified into High/Medium/Low severity for easy prioritization, and you can click through to see detailed test reports.

## Fix vulnerabilities
If you found issues, Snyk will help you fix them with the click of a “Fix” button.

TODO: screenshot of remediation PR

This click will generate a Pull Request with the minimal changes needed to fix the issue and get back to writing code. Where possible, Snyk will find the minimal direct upgrade you can apply to get a non-vulnerable version of the package in question. If you can't upgrade, Snyk will aim to patch the vulnerability using [open source patches from its VulnDB](https://github.com/Snyk/vulndb/).

## Prevent adding vulnerable packages
Once you're free of vulnerabilities, you need to make sure you don't add new vulnerable packages as your application evolves. To help with that, Snyk integrates its test directly into your Pull Request tests, catching vulnerable packages before they truly enter your application.

TODO: Screenshot of test in PR

## Respond to newly disclosed vulnerabilities
New vulnerabilities are disclosed each month, uncoverting previously unknown security holes in your application. Snyk helps you quickly respond to those issues by tracking and remembering your dependencies, and alerting you as soon as a new disclosure affects you.

You and your team will get an email notification with all the details, and Snyk will also submit a pull request with the fix straight to your project, using the same pull request described above.
