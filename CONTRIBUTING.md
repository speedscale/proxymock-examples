# Contributing to proxymock Snapshots

Hey there, intrepid engineer! 🛠️
So, you've found your way to this repository, and now you're thinking,

*"I love not writing mocks and integration tests, I'd like to help others avoid doing work just like me!"*

Good news—you absolutely can! 🎉

## 📸 What Are Snapshots? 
Snapshots are recordings of API requests to cloud services like **AWS DynamoDB, S3, BigQuery, or BigTable**. Think of them as **time capsules of API interactions**—except instead of burying them in your backyard, we use them to **mock APIs like a boss** with **[proxymock](https://docs.speedscale.com/proxymock/getting-started/)**.

By contributing snapshots, you’re helping fellow engineers develop and test their apps *without actually* hitting cloud services (because surprise bills are no joke).  

## ✨ How to Contribute a Snapshot  

1. **Install proxymock**
   If you haven't yet, install proxymock. The best way is to follow the [installation](https://docs.speedscale.com/proxymock/getting-started/installation/) guide. However, if you're impatient like us, you can do it in one simple command:

   ```sh
   brew install speedcale/tap/proxymock
   ```
   
   Now run proxymock:
   ```sh
   proxymock run
   ```

	Follow the directions output by this command and run your app in a new terminal. proxymock will capture API calls and automatically generate a snapshot file.

1.	Verify Your Snapshot
	Before you send your snapshot into the wild, check it:

	```sh
	proxymock inspect [snapshot-id]
	```

	* Ensure it’s anonymized (no AWS credentials, no PII, no embarrassing payloads).
	* Keep it small but useful—nobody wants a 500MB JSON file full of duplicate requests.

1.	Submit a PR
	* Fork the repo.
	* Add your snapshot to the appropriate directory (snapshots/aws/, snapshots/google/, etc.).
	* Update README.md if necessary.
	* Open a Pull Request with a descriptive title, like:
	feat: Add DynamoDB snapshot for batch write operations
	* Include a friendly description:
	* What API calls are in the snapshot?
	* Any edge cases covered?
	* Any oddities we should know about?
	5.	Await Feedback & Profit
Our friendly maintainers will review your contribution. If your snapshot passes the vibe check, it’ll be merged, and the world will be a better place. 🌎✨

⸻

❌ What Not to Do

🚫 No secrets. Ever. Double-check that you haven’t included access tokens, API keys, or your Netflix password.
🚫 No megafiles. If your snapshot is larger than a decent GIF, consider trimming it down.
🚫 No garbage data. If your snapshot is just a 404 Not Found response… thanks, but no thanks.

⸻

❤️ Thank You

We’re engineers too, and we get it—mocking APIs should be less painful than debugging a multi-region outage at 2 AM. Your contribution makes proxymock more powerful, more useful, and more awesome.

Welcome aboard, and happy snapshotting! 🚀
