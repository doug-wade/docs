---
title: ""
---

* Get started with our __<a href="https://snyk.io/docs/quick-start/" title="Quick start guide">step-by-step guide.</a>__
* Check our <a href="https://snyk.io/docs/using-snyk/" title="Using Snyk"> __detailed documentation for using Snyk.__</a>

Need help with anything you can’t find here? [Drop us a line](mailto:support@snyk.io) and we’ll get right back to you.

## CLI commands overview

```console
snyk [options] [command] [package]
```

The package argument is optional. If no package is given, Snyk will run the command against the current working directory allowing you test you non-public applications.

### Commands

```console
auth [api-token].....sign into snyk.
test ............... test for any known vulnerabilities.
wizard ............. configure your policy file to update, auto patch and ignore vulnerabilities.
protect ............ protect your code from vulnerabilities and optionally suppress specific vulnerabilities.
monitor ............ record the state of dependencies and any vulnerabilities on snyk.io.
policy ............. display the Snyk policy for a package.
```

### Options

```console
--dev .............. include devDependencies (defaults to production only)
--ignore-policy .... ignores and resets the state of your policy file
--trust-policies ... applies and uses ignore rules from your dependencies's Snyk policies, 
                     otherwise ignore policies are only shown as a suggestion.
--dry-run .......... don't apply updates or patches during protect.
-q, --quiet ........ silence all output.
-h, --help ......... this help information.
-v, --version ...... the CLI version.
```

### Examples

```console
snyk test
snyk test ionic@1.6.5
```

<div class="alert alert--inline">
  <p>Use `snyk test` in your test scripts. If a vulnerability is found, the process will exit with a non-zero exit code.</p>
</div>
