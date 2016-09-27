---
title: Configure Bitbucket Pipelines
---

After running the steps above to create a `.snyk `policy file, you now need to create a `bitbucket-pipelines.yml` file which will configure Bitbucket Pipelines.

1. On Bitbucket, add the Bitbucket Pipelines addon and enable it for the repository in question.
2. Use the `bitbucket-pipelines.yml` from [the snyk-pipelines repository](https://bitbucket.org/johannakoll/snyk-pipelines/src).

### Adapting an existing `bitbucket-pipelines.yml` file

If you want to adapt an existing `bitbucket-pipelines.yml` file, you should add the following line just after the `npm test` step:

```yaml
- node node_modules/snyk/cli protect
```

This will ensure that any patches you chose during `snyk wizard` are applied. The command `snyk test` will automatically run as part of `npm test` and will fail the pipeline if any known vulnerabilities are found in the dependencies.

A key value Snyk provides are our alerts when newly disclosed vulnerabilities affect your project's dependencies. 
To make sure the list of dependencies we have for your project is up to date, refresh it continuously by running `snyk monitor` in your deployment process. You'll also need to authenticate to Snyk, so we know where to update the dependencies.

To do both, add the following lines before the `npm test` step:

```yaml
- node node_modules/snyk/cli auth <SNYK_TOKEN>
- node node_modules/snyk/cli monitor
```

Configure your environment to include the `SNYK_TOKEN` environment variable. You can find your API token in your [account settings on snyk.io](https://snyk.io/account/). 
