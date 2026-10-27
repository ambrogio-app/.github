<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo-dark.svg">
    <img src="logo-light.svg" alt="Ambrogio" width="320">
  </picture>
</p>

# Ambrogio

**Ambrogio** is an open source home assistant that you host yourself, for example in your homelab. Members of the family talk to it by typing or by voice, from any room and from any device. Ambrogio keeps the conversation history in PostgreSQL and hands each request to the AI agent best suited to it.

## Your models, your agents

You choose each piece:

- **Language model**: each agent has its own provider, model and options: Mistral, OpenAI, Anthropic, Google, or any API compatible with OpenAI's Chat Completions.
- **Agents**: as many specialised agents as you want, each with its own instructions and, optionally, an MCP server that gives it tools, for example Home Assistant. An orchestrator picks the right agent for every request.
- **Memory**: the Memory agent searches the family's past conversations through an MCP server that the backend itself provides, to answer questions such as when something was planned or what was said.
- **Speech recognition**: the bundled Nemotron streaming model recognises Italian and English while you speak; another [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) streaming transducer model can replace it.
- **Voice**: the bundled Italian and English [Piper](https://github.com/k2-fsa/sherpa-onnx/releases/tag/tts-models) voices, or another Piper voice that you mount.
- **Wake word**: any word you write as text, chosen per satellite, without training a model.

The installation chooses the language, Italian or English: the agents answer in it and the backend speaks it. The texts Ambrogio writes itself, in the backend, the terminal client and the web chat, are available in English and Italian. The satellite speaks no messages of its own: it signals problems with a tone.

> Ambrogio is in early development. The configuration format may still change between versions.

## Repositories

| Repository | Role |
|---|---|
| [ambrogio-model](https://github.com/ambrogio-app/ambrogio-model) | Product capabilities, shared decisions and the workspace scripts of the Reqvire model spread over the repositories |
| [ambrogio-backend](https://github.com/ambrogio-app/ambrogio-backend) | Conversation server, agents, speech, PostgreSQL archive, Memory MCP server, public protocol |
| [ambrogio-cli](https://github.com/ambrogio-app/ambrogio-cli) | Terminal chat client |
| [ambrogio-satellite](https://github.com/ambrogio-app/ambrogio-satellite) | Voice satellite with wake word, microphone and speaker |
| [ambrogio-web](https://github.com/ambrogio-app/ambrogio-web) | Optional web chat client |
| [ambrogio-docs](https://github.com/ambrogio-app/ambrogio-docs) | User documentation site |
| [ambrogio-homelab-example](https://github.com/ambrogio-app/ambrogio-homelab-example) | Example home installation: one Compose file per service and the agents that use them |

## Documentation

Installation, configuration and architecture are documented at <https://ambrogio-app.github.io/ambrogio-docs/>.
