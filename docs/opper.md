# Using Opper

[Opper](https://opper.ai) is a European AI gateway with an OpenAI-compatible API. It gives access to 700+ models from 50+ providers (Anthropic, OpenAI, Google, Mistral, open-weight models, and more) with a single API key.

## Getting an API key

1. Sign up on the [Opper platform](https://platform.opper.ai)
2. Create an API key in the **API Keys** section

## Configuring Jupyter AI Lite to use Opper

Configure the [Generic provider (OpenAI-compatible)](./usage.md#using-a-generic-openai-compatible-provider) with the following settings:

- **Base URL**: `https://api.opper.ai/v3/compat`
- **Model**: a [model ID supported by Opper](https://opper.ai/models), for example `claude-sonnet-4-6` or `gpt-5.5`
- **API Key**: your Opper API key

:::{note}
A model ID such as `claude-sonnet-4-6` lets Opper pick a provider that serves the model. To use one provider only, prefix the model ID with it, for example `anthropic/claude-sonnet-4-6`.
:::

:::{note}
The Generic provider does not fetch the list of models. With the secrets manager, its API key is shared by all the Generic provider configurations, see [API Key Management](./api-keys.md).
:::
