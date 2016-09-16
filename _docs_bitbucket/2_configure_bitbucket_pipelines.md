---
title: Configure Bitbucket Pipelines
---

After running the steps above to create a `.snyk `policy file, you now need to create a `bitbucket-pipelines.yml` file which will configure Bitbucket Pipelines.

1. On Bitbucket, add the Bitbucket Pipelines addon and enable it for the repository in question.
2. Use the `bitbucket-pipelines.yml` from [the snyk-pipelines repository](https://bitbucket.org/johannakoll/snyk-pipelines/src).

If you want to adapt an existing `bitbucket-pipelines.yml` file, you should add the following line just before the `npm test` step:

```yaml
- node node_modules/snyk/cli protect
```

This will ensure that any patches you chose during `snyk wizard` are applied. The command `snyk test` will automatically run as part of `npm test` and will fail the pipeline if any known vulnerabilities are found in the dependencies.
