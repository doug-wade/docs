---
title: Patch and Protect
---

Patch and Protect

The next issue the wizard reports on our demo app is different.

```
? High severity vulnerability found in handlebars@3.0.3, introduced via snyk-demo-child@0.0.1
- from: snyk-demo-child@0.0.1 > handlebars@3.0.3
- info: https://snyk.io/vuln/npm:handlebars:20151207
  Remediation options (Use arrow keys)
❯ Patch (modifies files locally, updates policy for `snyk protect` runs)
  Set to ignore for 30 days (updates policy)
  Skip
```
_Patch handlebars prompt_

Snyk found a vulnerability in handlebars, pulled in via the direct dependency `snyk-demo-child`. Although the vulnerability [was fixed](https://snyk.io/vuln/npm:handlebars:20151207) in handlebars 4.0.0, `snyk-demo-child` has not upgraded to that version – so you can’t upgrade the vulnerability away.

This scenario is especially common in recently disclosed vulnerabilities, as it takes a while for the dependency chain to catch up. In addition, sometimes an upgrade is available, but it’s a major upgrade with breaking changes, and you can’t handle it right now. In cases when you have no upgrade option, instead of simply remaining vulnerable, Snyk suggests you patch the vulnerability with a Snyk patch.

After we patch Handlebars, the wizard prompts about two instances of uglify-js vulnerabilities, suggesting you patch them all.

```
? 2 vulnerabilities introduced via uglify-js
- info: https://snyk.io/package/npm/uglify-js/2.3.6
  Remediation options (Use arrow keys)
  Upgrade (no sufficient upgrade available, we'll notify you when there is one)
❯ Patch the 2 vulnerabilities
  Review the vulnerabilities separately
  Set to ignore for 30 days (updates policy)
  Skip
```
_Patch uglify prompt_

As projects expand, it’s common to find the same package repeated in the dependency tree, and it’s not that rare for one package to have multiple vulnerabilities. When the wizard sees multiple instances of a vulnerable package, it offers a shortcut to patch them all to save time. You can still choose to review and patch each issue separately, and if an instance was sufficiently upgraded by previously chosen upgrades it won’t be touched.

Note the wizard only patches the _locally installed_ files. This means you need to reapply this patch every time dependencies are reinstalled, which you can do by running `snyk protect`. The wizard stores the patches you chose in the Snyk policy (_.snyk_), and `snyk protect` will apply those patches, and those patches alone – it never unilaterally applies a patch. Each time you reinstall your dependencies, you should run `snyk protect` to close the vulnerabilities. The wizard can do this for you, as we’ll see later on.
