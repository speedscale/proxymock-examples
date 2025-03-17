<div align="center">
<img src="./resources/examples-logo.webp" height="300" alt="Mock Server (courtesy of AI)">
</div>
<br/>
<div align="center">
</div>

# proxymock service examples

Use the examples in this repository as pre-built mock servers or simulators for common APIs (or services) like AWS or GCP. Each example will runs a mock server that will serve responses like the real API.

## ⬇️ Installation

1. **Install proxymock**

   If you haven't yet, install proxymock. The best way is to follow the [installation](https://docs.speedscale.com/proxymock/getting-started/installation/) guide. However, if you're impatient like us, you can do it in one simple command:

   ```sh
   brew install speedcale/tap/proxymock
   proxymock init
   ```

   Note that proxymock automatically decodes TLS traffic if given permission. You will be asked to modify your local keystore to allow this optional feature. This is a good spot to point out that proxymock does not send data (other than telemetry) to any third party. Feel free to disallow anyway as non-TLS will still work.

1. **Pick a Snpashot**

    Pick the appropriate *.jsonl* from this repository. Import it into proxymock with the following command:

    ```sh
    proxymock import --file foo.jsonl
    ```
    Take note of the imported snapshot ID from the output.

## 📊 Usage

1. **Start Mock Server**

    ```sh
    proxymock run --snapshot-id [id]
    ```

1. **Run Your App**

    If your outbound calls respect environment variables, you should paste the following into the terminal you run your app in:

    ```sh
    export http_proxy=http://localhost:4140
    export https_proxy=http://localhost:4140
    ```

    If your app uses civilized SDKs then it will cause your app to redirect outbound traffic to the mock server. If this doesn't work you need to find the right environment variables for the app you use or modify the endpoints in your code.


## 📏 Limitations

* Mocks are not language dependent since they are network servers. Major revisions of an API may require a different snapshot. For instance, v2 of the AWS API has a different network format than v1.
* This repository contains the formatting and stub data necessary for each mocked service, but will want to modify the mocks to add realistic responses for your app. You can do that by modifying the *.jsonl*. Pro users can also record from a live environment (see [enterprise features](https://speedscale.com)).

## 📸 What Are Snapshots? 
Snapshots are recordings of API requests to cloud services like **AWS DynamoDB, S3, BigQuery, or BigTable**. Think of them as **time capsules of API interactions**—except instead of burying them in your backyard, we use them to **mock APIs like a boss** with **[proxymock](https://docs.speedscale.com/proxymock/getting-started/)**.

## License

This project is licensed under the Apache 2.0 License - see the [LICENSE](./LICENSE) file for details.

## 🛠 Contributing

Please visit our [contributions](./CONTRIBUTING.md) page for more information.