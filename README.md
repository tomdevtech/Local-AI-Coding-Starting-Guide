__TOC__

# Local-AI-Coding-Starting-Guide

During my research for local coding, I stumbled on this 4 tools. In this repo I want to present an overview of possible ways to combine them and get the best out of everything. Futermore you are welcome to try everything and leave a comment or suggestions!

This repo is meant as a continuing project, so don't see it as non plus ultra for local coding... It's an entry point for software engineers, AI engineers and many more who are interested in having the power of your coding on local machines. 

**Note:**

## Starting Tools

| Tool | Purpose | Description |
|---|---|---|
| **Ollama** | Local model backend (inference server) | Runs open-weight LLMs on your own hardware.|
| **LM Studio** | Local model backend (inference server) | Desktop app for browsing, downloading, and serving GGUF/MLX models with a graphical model catalog.|
| **Claude Code** | Coding agent | Anthropic's own agentic coding tool (CLI + VS Code extension). Speaks the Anthropic Messages API. By default it talks to Claude models over Anthropic's cloud API, but it can be redirected to any endpoint, including Ollama or LM Studio. |
| **Hermes Agent** | Coding / general-purpose agent | Nous Research's open-source (MIT), provider-agnostic autonomous agent. Runs as a persistent daemon with cross-session memory and self-created skills, switches between cloud and local providers with no lock-in and is able to attach to editors.|
| **LM Studio Bionic** | Standalone coding / work agent for open models | A separate app from LM Studio itself, but model downloading and management are built in, so it works on its own without needing the classic LM Studio app. Bundles its own agent harness, Code projects and Work projects, inline diffs, local codebase inspection, document/PDF/slide editing, on top of the LM Studio runtime. Runs fully local, or hands heavier tasks to LM Studio's own "Secure Cloud". |

## The Mental Model: Two Layers

- **Backend layer** (the "brain"): Ollama and LM Studio load model weights and run inference.
- **Agent layer** (the "hands"): Claude Code and Hermes Agent read your repo, write patches, run terminal commands, and orchestrate multi-step work. They need a backend to think with, whether that's a cloud API or  in our case, a local server.
