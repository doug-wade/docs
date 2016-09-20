---
title: "Snyk’s process for creating patches"
---
Patches are created and maintained by Snyk. If the package owner has made code changes to fix the issues, our patch is based on this official fix, and we remove any cosmetic or unrelated changes. If a package owner has not addressed the vulnerability yet, we write a patch from scratch.

Before releasing it, we verify the patch, backport it to older versions, and test that the patch hasn’t broken functionality.

The patches are a part of [Snyk’s open source vulnerability database](https://github.com/Snyk/vulndb/), so you can check them out before applying them. For example, the patches for the [ms ReDoS vulnerability](https://github.com/Snyk/vulndb/tree/master/data/npm/ms/20151024).
We don’t have patches for every case - if you need one that’s missing, <a href="mailto:contact@snyk.io">let us know</a>. We also [accept pull requests](https://github.com/Snyk/vulndb/blob/master/CONTRIBUTING.md)!
