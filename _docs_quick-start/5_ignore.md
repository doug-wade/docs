---
title: Ignore
---

This issue the wizard shows is not as easily solved.

```console
? Medium severity vulnerability found in validator@3.1.0, introduced via azure-mgmt-storage@0.9.16
- from: azure-mgmt-storage@0.9.16 > azure-common@0.9.11 > validator@3.1.0
- info: https://snyk.io/vuln/npm:validator:20130705
  Remediation options (Use arrow keys)
  Upgrade (no sufficient upgrade available, we'll notify you when there is one)
  Patch (modifies files locally, updates policy for `snyk protect` runs)
❯ Set to ignore for 30 days (updates policy)
  Skip
```
_Validator vulnerability_

A vulnerability is found in a deep `validator` dependency, which has neither an upgrade nor a patch available. There are many combinations of vulnerability and module versions, and not all of them can be patched. Snyk’s security team is constantly adding more patches to the [open source VulnDB](https://github.com/Snyk/vulndb) and would [welcome pull requests](https://github.com/Snyk/vulndb/blob/master/CONTRIBUTING.md), but some issues still have no patch.

There’s no easy fix for these issues. You’ll need to better understand the risk this issue presents to your system, and weigh this risk against the effort of fixing the issue – for instance, by removing the dependency. While you consider your actions, you can ‘snooze’ the issue with Snyk, telling it to ignore the issue for 30 days. Snyk will prompt you to provide a reason for ignoring, to help you remember why you did it later on.

```console
? Medium severity vulnerability found in validator@3.1.0, introduced via azure-mgmt-storage@0.9.16
- from: azure-mgmt-storage@0.9.16 > azure-common@0.9.11 > validator@3.1.0
- info: https://snyk.io/vuln/npm:validator:20130705
  Remediation options Ignore
? [audit] Reason for ignoring vulnerability? (None given) Not deployed to production
```
_Validator ignore reason_

If you assess the vulnerability and decide it’s not an issue (for instance, because a component is not really deployed to production), you can manually edit the Snyk policy (_.snyk_) file to use a far-future expiry date for this instance. Note that Snyk does not test devDependencies by default, avoiding most such red herrings.

In addition to any action you take, Snyk will let you know when a patch or upgrade become available for this scenario, so you can apply a better solution.
