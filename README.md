<div align="center">
<img src="./resources/examples-logo.webp" height="300" alt="Mock Server (courtesy of AI)">
</div>
<br/>
<div align="center">
</div>

# proxymock service examples

This repository contains bootstrapped mocks of backend services for use with the free [proxymock](https://proxymock.io) tool. The intent is to save you from having to understand and mock popular services like AWS DynamoDB, Google BigQuery, etc.  Each file in this repository represents a recording of a real service that you can tune to your needs without having to write a service mock. You can modify existing calls and fill in your own data but the structure of the calls is already in place. The process is much easier than making a custom mock (with realistic data).

Mocks are not language dependent since they are network servers. Major revisions of an API may require a different snapshot. For instance, v2 of the AWS API has a different network format than v1.

This repository contains the formatting and stub data necessary for each mocked service, but you need to have proxymock installed (it's free). You can do that by fallowing the [Getting Started](https://docs.speedscale.com/proxymock/getting-started/) or just run the following commands:

```sh
brew install speedscale/tap/proxymock
proxymock init
```

Navigate to one of the child folders in this repo matching the service you would like to mock. The data necessary for the mock is stored in a *.jsonl* file. Once you have your snapshot handy, turn it into a mock server like this:

```sh
proxymock import --file fancy-snapshot.jsonl
proxymock run --snapshot-id [insert uid printed by the previous command]
```


```sh

```