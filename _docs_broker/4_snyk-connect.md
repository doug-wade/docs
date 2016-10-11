---
title: "Connect Snyk to your brokered GitHub Enterprise / GitHub"
---

Once your broker client is up and running, you can connect you Snyk account to your GitHub Enterprise.

 1. **Important:** log out of [https://snyk.io]
 2. log in to [https://snyk.io]
 3. select the organisation that you're using with your broker
 4. navigate to the "Projects" page
 5. click on "Test my GitHub repositories"
 6. you will be prompted for GitHub permissions, which must be provided. This is required while the broker is in early-access, but this access *is not used*
 7. you should see repositories from your brokered GitHub Enterprise / GitHub

If you do not see any repositories, you may need to click the "Re-sync" button.

If you see your GitHub.com repositories then log out, then log back in and try again.

If you have access to both brokered and non-brokered Snyk organisations then you may need to "Re-sync" the first time you test repositories for each organisation.

[custom proxy]: https://github.com/Snyk/broker
[https://github.com/settings/tokens]: https://github.com/settings/tokens
[https://github.com/Snyk/broker-snyk-client-example]: https://github.com/Snyk/broker-snyk-client-example
[https://snyk.io]: https://snyk.io
[snyk.io]: https://snyk.io
[support@snyk.io]: mailto:support@snyk.io
