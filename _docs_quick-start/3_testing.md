---
title: Testing
---

To find vulnerabilities, the wizard will traverse the local project and collect the packages it uses (note this means you should only run it after you run `npm install`). It then posts this list to the Snyk service, where they’re matched against Snyk’s [open source vulnerability database](https://github.com/Snyk/vulndb).

This test also can be performed by running `snyk test`, which is useful when integrating Snyk into your CI (more on that later).

Once the vulnerabilities are determined, the wizard will go through them and guide you through the remediation steps needed. It remembers the answers you give, and when the questions end it makes the changes you asked for.

### Let’s go through the findings on the snyk demo app.

You can see the wizard tells you how many vulnerabilities were found in how many dependencies.

The first vulnerability is a **high severity issue in a direct dependency called bassmaster**. There’s only so much detail we can share in a terminal, but you can use the [info link](https://snyk.io/vuln/npm:bassmaster:20140927) to get more information about the vulnerability itself.

```
? High severity vulnerability found in bassmaster@1.5.1, introduced via bassmaster@1.5.1
- info: https://snyk.io/vuln/npm:bassmaster:20140927
  Remediation options (Use arrow keys)
❯ Upgrade to bassmaster@1.5.2
  Patch (modifies files locally, updates policy for `snyk protect` runs)
  Set to ignore for 30 days (updates policy)
  Skip
```
_Upgrade bassmaster prompt_

In many cases, disclosed vulnerabilities are fixed shortly after they’re discovered, and all you need to do is upgrade to the relevant version. When that’s possible, upgrade is the cleanest and best way to address such a security bug. In the case of bassmaster, all we need to apply is a ‘fix’ upgrade.

Next, we see that a direct dependency, **falcor-router-demo@1.0.3**, introduced **multiple vulnerabilities**. The vulnerabilities in this case aren’t in the `falcor-router-demo` code, but rather in the dependencies it pulls in. This is a very common scenario, as most of the packages used by your application are actually pulled in indirectly.

Unfortunately, you can’t upgrade a deep dependency, both for technical reasons and for fear of breaking functionality. Your remediation step therefore is to upgrade the direct dependency, triggering the deep dependency upgrade. In this case, upgrading `falcor-router-demo` to version 1.0.5 (a ‘fix’ upgrade) will trigger the `qs` and `semver` upgrades you need to fix the vulnerabilities.

The wizard reports **multiple vulnerabilities in the hapi@10.5.0 dependency**. This typically happens when you are several versions behind the latest version, and in the meantime multiple vulnerabilities have been found and fixed. In this case, clicking [the info link](https://snyk.io/test/npm/hapi/10.5.0) will show you details for the vulnerabilities that affect hapi.

```
? 7 vulnerabilities introduced via hapi@10.5.0
- info: https://snyk.io/package/npm/hapi/10.5.0
  Remediation options (Use arrow keys)
❯ Upgrade to hapi@11.1.4 (potentially breaking change, triggers upgrade to moment@2.11.2)
  Review vulnerabilities separately
  Set to ignore for 30 days (updates policy)
  Skip
```
_Upgrade hapi prompt_

The wizard’s default suggestion is to upgrade to the latest version, addressing all issues, but you can also choose to review and act on each vulnerability separately.
