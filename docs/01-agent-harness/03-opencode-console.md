# OpenCode Console

[OpenCode Console](https://opencode.ai/console/) is a suite of hosted
services from the team that develops the [OpenCode agent](https://opencode.ai/).
It provides access to a large catalog of AI coding models, including free
models, so you can complete this course without paying for a model provider.

You can use Console's free models without authenticating, but signing in is
recommended because some features require an account.

OpenCode can also connect directly to other providers. If you already have a
ChatGPT, Google Gemini, Claude, or another provider account, use that provider.
If you do not have a preference, OpenCode Console is a convenient way to start
with a free model.

## Connect a provider

Inside an OpenCode session, run [`/connect`](https://opencode.ai/v2/docs/providers)
to connect OpenCode to a provider such as OpenCode Console or ChatGPT:

```text
/connect
```

Follow the prompts to choose the provider and complete its authentication, if
required.

## Choose a model

Run [`/models`](https://opencode.ai/v2/docs/models) to open the model selector.
Search for a model, then select it to switch models.

## Recommended free model

If you do not already have a preferred provider—for example, a Claude account
with an API key or a ChatGPT account with a paid subscription—we recommend
[DeepSeek V4.1 Flash Free](https://opencode.ai/v2/docs/console/models#free-models)
through OpenCode Console.

This endpoint is available for a limited time. OpenCode states that the
provider retains no request data and does not use it to train models. Even so,
do not send private information, credentials, or other sensitive data through
it.