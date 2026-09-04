# Free agentic-AI

The goal of this meetup is to help you get started using an agentic-AI workflow for free.

At the end of this meetup, you will be able to do things like this:

* Explain what an agent and an LLM are and which types exist.
* Install a popular open source agent and run free models, online and locally.

## Who is the audience?

* Anyone who wants to start using AI-agents, e.g. data scientists and software developers.

## Why is it important?

The current cost of agentic-AI tools keeps many people from embracing an important workflow.

## Objectives

* Understand what an agent, what an LLM is, and what types there are.
* Install a popular open source agent and use it with free models, online and locally.

## Demo

### Agents and models

What an agent is, what an LLM is, and which types exist.

* Agents are systems where LLMs dynamically direct their own processes and tool usage, as opposed to workflows with predefined code paths. Short version: LLMs autonomously using tools in a loop. Shortest: agent equals LLM plus harness. Diagrams: <https://www.anthropic.com/engineering/building-effective-agents>
* Types, paid vs free: <https://models.dev> (free entries show $0.00; OpenCode Zen needs billing details per <https://opencode.ai/docs/providers/>).
* Types, size and context: tinyllama at 1.1B and 638MB with 2K context (<https://ollama.com/library/tinyllama>) against 27b and 30b entries with 128K and larger contexts (<https://ollama.com/search?c=tools>, <https://ollama.com/library/llama3.2>).
* Quotas: open the provider rate-limits page live at demo time and read the free-tier numbers there. No numbers frozen in these materials.

### Installing and running free

Install a popular open source agent and run free models, online and locally.

Try it in a docker container mounted at your working directory:

```
docker run -it --rm -w /demo -v "$(pwd):/demo" ghcr.io/anomalyco/opencode
```

Or install it in your system:

```
curl -fsSL https://opencode.ai/install | bash
```

More options at <https://opencode.ai/docs>.

Gotchas from a live run: minimal containers may lack curl, so run `apt-get update && apt-get install -y curl` first. After installing, reload the shell with `source ~/.bashrc` before running `opencode`.

```
/connect
/models
```

Pick a $0.00 entry from <https://models.dev> at demo time.

```
ollama launch opencode
```

Download ollama at <https://ollama.com/download>. On Linux or macOS, paste this in the terminal:

```
curl -fsSL https://ollama.com/install.sh | sh
```

On Windows, paste this in PowerShell:

```
irm https://ollama.com/install.ps1 | iex
```

Contrast `ollama run tinyllama` (chat only, 2K context, below the 64k opencode minimum) with `ollama launch opencode --model llama3.2` (documented tool use, 128K context). Model pages: <https://ollama.com/library/tinyllama>, <https://ollama.com/library/llama3.2>. Wiring reference: <https://docs.ollama.com/integrations/opencode>

## Resources

* opencode: <https://opencode.ai>
* Project: [GitHub repository](https://github.com/anomalyco/opencode)
* Models.dev: [75+ LLM providers](https://models.dev)
* Ollama and opencode: [integration docs](https://docs.ollama.com/integrations/opencode)
* Agents, defined: [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)
