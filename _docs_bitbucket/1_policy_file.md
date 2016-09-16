---
title: Creating a policy file
---

1. Install the Snyk utility using `npm install -g snyk`.
2. Run `snyk wizard` in the directory of your project following the prompts which will also generate a `.snyk` policy file.
3. Ensure the `.snyk` file you generated was added to your source control (`git add .snyk`).
4. If you selected to, Snyk will include `snyk test` as part of your `npm test` command, so if there are new vulnerabilities in the future, BitBucket pipelines will fail.
