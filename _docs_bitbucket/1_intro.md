---
title: Bitbucket Pipelines and Snyk integration
---

By integrating Snyk into [Bitbucket Pipelines](https://bitbucket.org/product/features/pipelines), you can continuously monitor your codebase for known vulnerabilities in your dependencies.

Here are the steps required to set it up:

### Step 1

1. Install the Snyk utility using `npm install -g snyk`.
2. Run `snyk wizard` in the directory of your project following the prompts which will also generate a `.snyk` policy file.
3. Ensure the `.snyk` file you generated was added to your source control (`git add .snyk`).
4. If you selected to, Snyk will include `snyk test` as part of your `npm test` command, so if there are new vulnerabilities in the future, BitBucket pipelines will fail.

### Step 2

On Bitbucket, add the Bitbucket Pipelines addon and enable it for the repository in question.

Use the `bitbucket-pipelines.yml` from [the snyk-pipelines repository](https://bitbucket.org/johannakoll/snyk-pipelines).

If you want to adapt an existing `bitbucket-pipelines.yml` file, you should add the following lines to `pipelines.default.step.script`, before `npm test`:

```yaml
# install the snyk module
- npm install -g snyk
# run snyk protect to apply any patches
- snyk protect
```

### Step 3

Enable pipelines

Bitbucket Pipelines will now apply any patches you specified when you ran `snyk wizard` and will pass if there are no known vulnerabilities in your dependencies, or fail if any are found.

For more information about using the Snyk CLI, read [the documentation on Snyk CLI](/docs/using-snyk/)
