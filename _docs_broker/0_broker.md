---

---

<div class="alert alert--inline alert--notice">
  <p class="alert__text">
    [Insert some text about Snyk Broker]
  </p>
</div>

These instructions will get you up and running with a Snyk broker, allowing your private GitHub Enterprise to connect to Snyk.io. A Snyk broker can also be used between Snyk and github.com itself.

## GitHub / GitHub Enterprise setup

In order to interact with your GitHub repositories, Snyk needs to use a GitHub personal access token with "repo" and "admin:repo_hook" scopes.

To create a GitHub token:
 1. log in to your GitHub Enterprise (or github.com, if that's what you're brokering)
 2. navigate to "/settings/tokens" in your web browser. e.g. for github.com, go to https://github.com/settings/tokens
 3. click on the "Generate new token" button
 4. enter a description for the token, and select the "repo" and "admin:repo_hook" scope
 5. click on the "Generate token" button
 6. save the token so that you can configure your broker with it

This GitHub token must be provided to the broker client, which then inserts it into requests as they are proxied from Snyk to your GitHub servers.

*The GitHub token never leaves your network!*

## Broker client

The broker client is a web server which securely relays requests between Snyk's servers and your GitHub Enterprise. It needs to run on a network which has both outbound internet access and access to your GitHub Enterprise.

To set up and run a Snyk broker-client:

1. Install snyk-broker

     `$ npm install -g snyk-broker`

2. Initialise the broker for use with Snyk

     `$ broker init snyk`

   This will generate two files:
     - ".env"        : the brokers configuration
     - "accept.json" : the rules used to filter the requests being proxied to and from the Snyk servers

3. Edit the ".env" file, providing the following details:

    | Variable name     | Description                                                                                                                                          |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
    | BROKER_TOKEN      | Your unique broker token, given to you by Snyk. **This is a private token and must not be shared.**                                                  |
    | GITHUB_TOKEN      | A GitHub personal access token for the user that Snyk will use to access your Github repositories.                                                   |
    | GITHUB            | The host (and port if necessary) of your private GitHub server.                                                                                      |
    | GITHUB_API        | The url to the api of your private GitHub server.                                                                                                    |
    | GITHUB_RAW        | The url to access raw contents of files in git repos on your private GitHub server                                                                   |
    | BROKER_CLIENT_URL | The url that your broker *client* is accessible at, which will be used for GitHub webhooks that notify Snyk of relevant changes to your repositories |

   Note: The .env file is generated with defaults appropriate for use with GitHub Enterprise. It also includes instructions for values to use with github.com.

4. Start the broker

    `$ broker client`

   The broker can be started in debugging mode with:

    `$ broker client --verbose`

   Note: your BROKER_TOKEN will be outputted on stdout when the broker is started with `--verbose`.

Alternatively, the broker can also be installed as part of a private npm package. See https://github.com/Snyk/broker-snyk-client-example for an example of this.
