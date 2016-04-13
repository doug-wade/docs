---
title: Integrating Snyk into your dev workflow
---

<p>To continuously avoid known vulnerabilities in your dependencies, integrate Snyk into your continuous integration (a.k.a. build) system. Here are the steps required to to so:</p>

1. Install the Snyk utility using `npm install -g snyk`.
2. Run `snyk wizard` in the directory of your project following the prompts which will also generate a `.snyk` policy file.
3. Ensure the `.snyk` file you generated was added to your source control (`git add .snyk`).
4. If you selected to, Snyk will include `snyk test` as part of your `npm test` command, so if there are new vulnerabilities in the future, your CI will fail, protecting you from introducing vulnerabilities to production. Alternatively, you can add `snyk test` to any other CI test platform you use.

If you monitor a project with Snyk, you'll get notified if your project's dependencies are affected by newly disclosed vulnerabilities. To make sure this list of dependencies is up to date, refresh it continuously by running `snyk monitor` in your deployment process. You'll also need to include your API key as an environment value. Find your API key on the dashboard after logging in.

Important note: do not check your API key into your source control, as it may expose it! 
Instead, use your CI environment variables to configure it. Most CIs have a page explaining how to do so, including [Travis](https://docs.travis-ci.com/user/environment-variables/), [Circle](https://circleci.com/docs/environment-variables/) and [Codeship](https://codeship.com/documentation/continuous-integration/set-environment-variables/). You can find others through an easy [Google search]( https://www.google.co.uk/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=setting+up+env+variables+in+CI).
