---
title: Using Snyk
---

### Why should I add Snyk Test to my Continuous Integration (CI)?

Integrating Snyk will prevent code changes from introducing new vulnerable packages. [Find out how to integrate Snyk into your workflow](https://snyk.io/docs/using-snyk/#integrating-snyk-into-your-dev-workflow).

### How can I use Snyk behind a proxy?

To run Snyk from behind a proxy you will need to use an enviroment value to point to your proxy. The following environment variables are respected by Snyk:

- `HTTP_PROXY` / `http_proxy`
- `HTTPS_PROXY` / `https_proxy`
- `NO_PROXY` / `no_proxy`

For example, to configure this as a one time value, you can run:

`$ https_proxy=https://my.corporate.proxy:8080/ snyk test`

### Why does Snyk install itself into my production dependencies?

After running `snyk wizard`, if you choose to protect upon installation of your package, Snyk will need to be bundled as a production dependency.

However, if you select to *only* test your page (and not protect), Snyk will install itself as a development dependency.

<h3 class="h4">How can I test a Github repository from the command-line interface tool (CLI)?</h3>

Currently, we support testing public Github repositories only.
To test a public Github repository, run snyk test and include the Github URL to the repo.

```zsh
snyk test https://github.com/snyk/snyk
```

The following git URL formats are supported:

* git://github.com/user/project.git#commit-ish
* https://github.com/user/project#commit-ish
* user/project#commit-ish

This also works for Bitbucket and GitLab.
You can also test a public npm package or Github project via the [Test page on snyk.io](https://snyk.io/test/).

### How can I delete my data?

You can delete a project on the project page on the Snyk website. This will delete the project, and all snapshots that are related to it, and you won’t be able to access it. Please note that the data remains in our database, so if you would like to restore it, let us know. If you would like us to delete your project data permanently from the database, <a href="mailto:support@snyk.io">email us</a> and we’ll sort it out.

### How can I delete my account?

Until we support deleting your account via the Snyk website, this is a manual process. <a href="mailto:support@snyk.io">Email us</a>, and we will remove your account and all your data from our database.

### What analytics do you track? How can I opt out?

We are using a range of web analytics tools to understand and analyse user behaviour on snyk.io. If you’d like to block tracking, use one of the many browser tools available.

Our CLI tool reports an event for each command to our analytics, including the version of the CLI tool, the User ID, and the package name. This allows us to better understand how the CLI client is used, and informs our product development decisions.

If you would like to opt out, you can do so by running the following command:

```zsh
snyk config set disable-analytics=1
```

To remove the flag, run:

```zsh
snyk config unset disable-analytics
```

If you have any questions or problems, please <a href="mailto:support@snyk.io">email us</a>.
