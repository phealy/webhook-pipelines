# Cross-repository GitHub pull request status check pipeline

This pipeline is designed to be triggered using an Azure Pipelines Incoming Webhook Service Connection from a GitHub repository based on a pull-request webhook. It will only act on actions that indicate code was changed, and will run one or more checkout tasks on the pull request head branch. It will then use the Azure Pipelines PAT to post a commit status back to GitHub, which allows it to be used as a protected branch check for pull requests.

**NOTE: you must manually trigger this pipeline once to register the
webhook before GitHub can trigger it.**

See [the pipeline file](github__pahealy7__apim-configuation__pr.yml) for more information; it has inline comments.

Documentation:

- [Azure Pipelines Incoming Webhooks](https://docs.microsoft.com/en-us/azure/devops/release-notes/2020/pipelines/sprint-172-update#generic-webhook-based-triggers-for-yaml-pipelines)
- [GitHub pull request webhook event](https://docs.github.com/en/developers/webhooks-and-events/webhook-events-and-payloads#pull_request)
