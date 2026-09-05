# Free agentic-AI

The goal of this meetup is to help you get started using AI-agents for free.

By the end of this meetup you'll have a workflow that will take you a long way before
feel the need to spend any money.

## Who is the audience?

Anyone who used to write code by hand and wants to try an agentic AI workflow
for free, e.g. data scientists and software developers.

## Why is it important?

The agentic AI workflow is increasingly popular.

## Objectives

* Understand what an AI-agent is.
* Learn about some of the most popular AI-agents today.
* Setup an AI-agent and use it with models on the cloud.
* Setup and use models locally.

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

You can also connect to a different model provider. For example, you may connect to free models from Google with:

```
/connect
```

You can get an API key from https://aistudio.google.com/api-keys

### Use opencode with a free ollama model running locally

You can use opencode to set this up for you, e.g.:

> Install ollama and guide me through the setup to download and use the smallest model that can be used for an agentic workflkow with opencode.

<details><summary>Or do it yourself</summary>

Install [ollama](https://ollama.com/download) for your OS, e.g.:

```
curl -fsSL https://ollama.com/install.sh | sh
```

Sign in with

```
ollama signin
```

Then [browse models](https://ollama.com/search) and pull one, e.g.:

```
ollama pull llama3.2:3b
```

And `/connect` it from inside opencode.

## Resources

* opencode: <https://opencode.ai>
* Project: [GitHub repository](https://github.com/anomalyco/opencode)
* Models.dev: [75+ LLM providers](https://models.dev)
* Ollama and opencode: [integration docs](https://docs.ollama.com/integrations/opencode)
* Agents, defined: [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)
* Augmented coding patterns: <https://lexler.github.io/augmented-coding-patterns/>
* [What is an agent](https://tidydesign.substack.com/p/what-is-an-agent)
* [Trusted mini-agents](https://trustedminiagents.dev/)


