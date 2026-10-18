<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo-dark.svg">
    <img src="logo-light.svg" alt="Ambrogio" width="320">
  </picture>
</p>

# Ambrogio

**Ambrogio** is an open source home assistant that you host yourself, for example in your homelab. Members of the family talk to it by typing or by voice, from any room and from any device. Ambrogio keeps the conversation history and hands each request to the AI agent best suited to it.

## Your language, your models, your agents

Ambrogio is not tied to one language or one set of models. You choose each piece:

- **Speech recognition**: any [Vosk](https://alphacephei.com/vosk/models) model, in the language you speak.
- **Voice**: any [Piper voice or Kokoro model converted for sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx/releases/tag/tts-models). With Kokoro you pick the voice and the language it reads. Two Italian Piper voices come bundled.
- **Wake word**: any [openWakeWord](https://github.com/dscripka/openWakeWord) model, including one you train yourself, chosen per satellite.
- **Language model**: each agent has its own model and options. Mistral is currently the only supported provider.
- **Agents**: as many specialised agents as you want, each with its own instructions and, optionally, an MCP server that gives it tools, for example Home Assistant. An orchestrator picks the right agent for every request.

Ambrogio answers in the language you write in the agents' instructions. Pair it with a recognition model and a voice for the same language. The texts Ambrogio writes itself, in the backend, the terminal client and the web chat, are available in English and Italian. The satellite speaks no messages of its own: it signals problems with a tone.

> Ambrogio is in early development. The configuration format may still change between versions.

## Repositories

| Repository | Role |
|---|---|
| [ambrogio-backend](https://github.com/ambrogio-app/ambrogio-backend) | Conversation server, agents, speech, storage, public protocol |
| [ambrogio-cli](https://github.com/ambrogio-app/ambrogio-cli) | Terminal chat client |
| [ambrogio-satellite](https://github.com/ambrogio-app/ambrogio-satellite) | Voice satellite with wake word, microphone and speaker |
| [ambrogio-web](https://github.com/ambrogio-app/ambrogio-web) | Optional web chat client |
| [ambrogio-docs](https://github.com/ambrogio-app/ambrogio-docs) | User documentation site |

## Documentation

Installation, configuration and architecture are documented at <https://ambrogio-app.github.io/ambrogio-docs/>.
