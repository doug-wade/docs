---
title: Security research
draft: false
---

<h3 class="h4">How do you find out about new vulnerabilities?</h3>

<p>We monitor existing node.js security portals and tools, such as <a href="https://nodesecurity.io/">Node Security Project</a>, the <a href="https://groups.google.com/forum/#!forum/nodejs-sec">nodejs-sec Google Group</a>, <a href="https://srcclr.com/">SRC:CLR</a>, or <a href="http://retirejs.github.io/retire.js/">Retire.js</a>. We also monitor Github activity and other online sources for new vulnerabilities.</p>

<h3 class="h4">Where does Snyk get patches from?</h3>

<p>Patches are created and maintained by Snyk. If the package owner has made code changes to fix the issues, our patch is based on this official fix, and we remove any cosmetic or unrelated changes. If a package owner has not addressed the vulnerability yet, we write a patch from scratch.</p>

<p>Before releasing it, we verify the patch, backport it to older versions, and test that the patch hasn’t broken functionality.</p>

<p>The patches are a part of <a href="https://github.com/Snyk/vulndb/">Snyk’s open source vulnerability database</a>, so you can check them out before applying them. For example, the patches for the <a href="https://github.com/Snyk/vulndb/tree/master/data/npm/ms/20151024">ms ReDoS vulnerability</a>. 
We don’t have patches for every case - if you need one that’s missing, <a href="mailto:contact@snyk.io">let us know</a>. We also <a href="https://github.com/Snyk/vulndb/blob/master/CONTRIBUTING.md">accept pull requests</a>!</p>
