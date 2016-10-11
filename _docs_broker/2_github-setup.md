---
title: "GitHub / GitHub Enterprise set-up"
---

In order to interact with your GitHub Enterprise repositories, Snyk needs to use a GitHub Enterprise personal access token with "repo" and "admin:repo_hook" scopes.

To create a GitHub Enterprise token:

 1. log in to your GitHub Enterprise (or github.com, if that's what you're connecting via the broker)
 2. navigate to "/settings/tokens" in your web browser. e.g. for github.com, go to [https://github.com/settings/tokens](https://github.com/settings/tokens)
 3. click on the "Generate new token" button
 4. enter a description for the token, and select the "repo" and "admin:repo_hook" scope
 5. click on the "Generate token" button
 6. save the token so that you can configure your broker with it

This GitHub token must be provided to the broker client, which then inserts it into requests as they are proxied from Snyk to your GitHub Enterprise.

*The GitHub token never leaves your network!*
