# Historical proxymock snapshots

This repository preserves API traffic recordings captured in 2025. The snapshots remain available for existing links, but we no longer maintain them as getting-started examples. The current files have authentication headers removed, but earlier Git commits may still contain the original recorded headers. The snapshots reflect the vendor APIs available when they were captured.

For a runnable proxymock example, use [speedscale/mock-lab](https://github.com/speedscale/mock-lab). It includes small apps in multiple languages, committed recordings, and guided exercises for recording, mocking, and replaying traffic. Start with its [README](https://github.com/speedscale/mock-lab#readme) or the [proxymock quickstart](https://docs.speedscale.com/proxymock/getting-started/quickstart/quickstart-cli/).

The historical recordings here cover OpenAI, Anthropic Claude, and AWS DynamoDB. We tested representative files with proxymock v2.5.1114: they import and serve recorded responses locally. That check does not establish compatibility with current vendor APIs or SDKs.

New runnable examples belong in [mock-lab](https://github.com/speedscale/mock-lab).
