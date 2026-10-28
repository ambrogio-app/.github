<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo-dark.svg">
    <img src="logo-light.svg" alt="Ambrogio" width="320">
  </picture>
</p>

# Ambrogio

**Ambrogio**: talk to it like Alexa, chat with it like ChatGPT — one self-hosted AI assistant for your whole homelab. Multi-agent by design: each agent you configure handles one job, such as the house, music, weather or your documents, using the services you already host.

Your family talks to it out loud from a voice satellite in each room, or types to it in a browser or a terminal, and every conversation is kept on your server and can be continued from any of them.

## Your models, your agents

You choose each piece:

- **Agents**: as many as you want, each with its own instructions and LLM, and optionally an [MCP](https://modelcontextprotocol.io/) server that gives it tools, such as Home Assistant. An orchestrator picks the right agent for every request. The backend also lets a Memory agent search your past conversations.
- **LLMs**: Mistral, OpenAI, Anthropic, Google, or any OpenAI-compatible server, including one running in your home. Each agent can use a different one.
- **Speech recognition and voice**: run on your server with [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx). A streaming Nemotron model for Italian and English and Piper voices come bundled; you can mount your own.
- **Wake word**: any word, written as text, with no training, chosen per satellite.

Ambrogio answers in English or Italian. No audio leaves your network, and with LLMs on your own server nothing does.

> Ambrogio is in early development. The configuration may still change between releases.

## Repositories

| Repository | Role |
|---|---|
| [ambrogio-backend](https://github.com/ambrogio-app/ambrogio-backend) | Conversation server, agents, speech, storage |
| [ambrogio-web](https://github.com/ambrogio-app/ambrogio-web) | Web chat |
| [ambrogio-cli](https://github.com/ambrogio-app/ambrogio-cli) | Terminal client |
| [ambrogio-satellite](https://github.com/ambrogio-app/ambrogio-satellite) | Voice satellite with wake word, microphone and speaker |
| [ambrogio-homelab-example](https://github.com/ambrogio-app/ambrogio-homelab-example) | A complete homelab installation, one Compose file per service |
| [ambrogio-docs](https://github.com/ambrogio-app/ambrogio-docs) | User documentation site |
| [ambrogio-model](https://github.com/ambrogio-app/ambrogio-model) | Product-wide engineering model |

## Documentation

Installation, configuration and concepts are documented at <https://ambrogio-app.github.io/ambrogio-docs/>.
