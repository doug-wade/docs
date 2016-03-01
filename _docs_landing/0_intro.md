---
title: ""
draft: true
---

Just getting started with Snyk? Follow this step-by-step guide to get set up.

Check our detailed documentation, and if you’d like to know more about how to tackle known vulnerabilities, our FAQ have all the answers.

Need help with anything you can’t find here? Drop us a line at support@snyk.io and we’ll get right back to you.

## CLI commands overview

```
snyk [options] [command] [package]
```

The package argument is optional. If no package is given, Snyk will run the command against the current working directory allowing you test you non-public applications.

### Commands

```
auth ............... sign into snyk (required).
test ............... test for any known vulnerabilities.
wizard ............. configure your policy file to update, auto patch and ignore vulnerabilities.
protect ............ protect your code from vulnerabilities and optionally suppress specific vulnerabilities.
monitor ............ record the state of dependencies and any vulnerabilities on snyk.io.
policy ............. display the Snyk policy for a package.
support ............ file an issue or request support.
```

### Options

```
--dev .............. include devDependencies (defaults to production only)
--ignore-policy .... ignores and resets the state of your policy file
--dry-run .......... don't apply updates or patches during protect.
-q, --quiet ........ silence all output.
-h, --help ......... this help information.
-v, --version ...... the CLI version.
```

### Examples

```
snyk test
snyk test ionic@1.6.5
```

<div class="alert alert--inline alert--notice">
  <p>use `snyk test` in your test scripts, if a vulnerability is found, the process will exit with a non-zero exit code.</p>
</div>
