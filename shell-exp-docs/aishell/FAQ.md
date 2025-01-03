---
title: AI Shell FAQ
description: Get answers to common questions about AI Shell.
ms.date: 11/11/2024
ms.topic: faq
---

# Frequently Asked Questions

This page provides help with common questions about AI Shell, also known as Project Mercury.

## What is Project Mercury?

**Project Mercury** was the code name for the project that created AI Shell. AI Shell includes a
framework for building your own AI Agents and assistance providers for an AI Shell. Agents provide
the user interface for interacting with LLMs and integrating with PowerShell 7. For more, see the
[AI Shell architecture][03].

## What operating systems are supported?

We've tested on macOS and Windows operating systems. **AI Shell** may work on linux but we haven't
tested it. We can't guarantee that all features will work as expected.

## What are the different ways I can use AI Shell?

You can use AI Shell in two ways:

- As a standalone application
- As a split pane experience in PowerShell 7 and Windows Terminal

The split pane experience is based on the capabilities of your terminal. terminal. For example, you
can split the Windows Terminal pane by running the following command: `wt -w 0 sp`. Refer to the
documentation for your terminal application to see if it supports this feature.

> [!NOTE]
> Not all terminal applications support this feature.

We've made this experience easier when using PowerShell 7 and Windows Terminal. For more information
see [Get started with AI Shell in PowerShell][05].

## What is the difference between the standalone application and the split pane experience?

The split pane experience with PowerShell 7 has deeper integration with PowerShell and thus can
communicate across the panes for inserting AI generated codes to the working shell and sending
errored commands to the AI pane for assistance. The standalone application is a more generic
experience that can be used with any shell and has no such integration.

## What are AI agents?

An agent is a code library that implements the interfaces that talk to a specific language model or
assistance provider. An assistance provider is an agent that provides user assistance without using
a language model or AI engine.

We currently support the following agents:

- **openai-gpt** - an agent for [**Azure OpenAI**][02]
- **azure** - an agent for [**Copilot in Azure**][01]

Users interact with these agents using natural language in a conversational manner.

## How do I create an agent?

To create an agent, you need to implement the `IAgent` interface. For more information, see
[Create an Ollama Agent][04] for the details of creating an agent.

## How do I share my agent or find other community built agents?

There isn't a centralized repository for sharing community built agents. In the interim, we
recommend sharing it on the [discussions page][06] of the Project Mercury repository.

<!-- link references -->
[01]: agent-azure.md
[02]: agent-openai.md
[03]: developer/agent-architecture.md
[04]: developer/create-ollama-agent.md
[05]: get-started-powershell.md
[06]: https://github.com/PowerShell/ProjectMercury/discussions/categories/agent-sharing
