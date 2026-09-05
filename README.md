# Free agentic AI

The goal of this meetup is to help you get started using AI agents for free.

By the end of this meetup you'll have a workflow that will take you a long way before
you feel the need to spend any money.

## Who is the audience?

Anyone who writes code by hand and wants to try an agentic AI workflow
for free, e.g., data scientists and software developers.

## Why is it important?

The agentic AI workflow is increasingly popular.
<!-- FIXME: Vague claim — add a source or make concrete (popular with whom, measured how?). -->

## Objectives

* Understand what an AI agent is.
* Learn about some of the most popular AI agents today.
* Set up an AI agent and use it with models on the cloud.
* Set up and use models locally.

## Contents

### Agents and models

> An AI agent ... is an artificial intelligence program that can pursue goals, use software or other tools, and take actions.
> -- [Wikipedia](https://en.wikipedia.org/wiki/AI_agent)

That artificial intelligence program (a.k.a. LLM or just model) is like a brain.
It can only chat with you. To take actions it needs additional software that
acts like a harness.

``` 
Agent = LLM + Harness
```

There are many [agents](https://www.morphllm.com/best-ai-coding-agents-2026) and
[models](https://llm-stats.com/leaderboards/best-ai-for-coding).

### Use opencode with a free model running on the cloud

Try opencode with:

```
docker run -it --rm ghcr.io/anomalyco/opencode
```

Or [install it](https://opencode.ai/docs) following the instructions for your OS, e.g.:

```
curl -fsSL https://opencode.ai/install | bash
```

Then use it with some of the free models from opencode running on the cloud:

```
/models
```

You can also connect to a different model provider. For example, you can connect to free models from Google with:
<!-- FIXME: Ambiguous — which Google models (names/quotas change often)? Specify or link the list. -->

```
/connect
```

You can get an API key from [Google AI Studio](https://aistudio.google.com/api-keys).

### Use opencode with a free Ollama model running locally

You can use opencode to set this up for you, e.g.:

> Install Ollama and guide me through the setup to download and use the smallest model that can be used for an agentic workflow with opencode.
<!-- FIXME: Ambiguous — "smallest capable model" changes over time. Name the model you tested or state how to choose one. -->

<details>
<summary>Or do it yourself</summary>

Install [Ollama](https://ollama.com/download) for your OS, e.g.:

```
curl -fsSL https://ollama.com/install.sh | sh
```

Then [browse models](https://ollama.com/search) and pull one, e.g.:

```
ollama pull llama3.2:3b
```

And `/connect` it from inside opencode.

</details>

## Resources

* opencode: <https://opencode.ai>
* Orca: [free, open-source agent IDE](https://www.onorca.dev/) ([MIT](https://github.com/stablyai/orca)) to run opencode and other agents in parallel worktrees.
* Agents, defined: [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)
* Augmented coding patterns: <https://lexler.github.io/augmented-coding-patterns/>
* [What is an agent](https://tidydesign.substack.com/p/what-is-an-agent)
* [Trusted mini-agents](https://trustedminiagents.dev/)


