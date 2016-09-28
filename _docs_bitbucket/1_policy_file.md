---
title: Creating a policy file
---

1. Install the Snyk utility using `npm install -g snyk`.
2. Run `snyk wizard` in the directory of your project following the prompts which will also generate a `.snyk` policy file. For more information about this, see [our CLI documentation](/docs/using-snyk/#wizard).
3. When asked by `snyk wizard`, select to include `snyk test` as part of your `npm test` command. If there are new vulnerabilities in the future, Bitbucket Pipelines will fail.
4. Ensure the `.snyk` file you generated was added to your source control (`git add .snyk`).

