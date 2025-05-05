---
title: "adk-python"
owner: "google"
source: "https://github.com/google/adk-python"
website: "https://google.github.io/adk-docs/"
description: "An open-source, code-first Python toolkit for building, evaluating, and deploying sophisticated AI agents with flexibility and control."
stars: 3.3
tags:
  - "inbox"
  - "github"
  - "repo"
created: 2025-04-11
---
## README

[![License](https://camo.githubusercontent.com/5ce2e21e84680df1ab24807babebc3417d27d66e0826a350eb04ab57f4c8f3e5/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c6963656e73652d4170616368655f322e302d626c75652e737667)](https://github.com/google/adk-python/blob/main/LICENSE)

# [![](https://github.com/google/adk-python/raw/main/assets/agent-development-kit.png)](https://github.com/google/adk-python/blob/main/assets/agent-development-kit.png)### An open-source, code-first Python toolkit for building, evaluating, and deploying sophisticated AI agents with flexibility and control.### Important Links: [Docs](https://google.github.io/adk-docs/) & [Samples](https://github.com/google/adk-samples).The Agent Development Kit (ADK) is designed for developers seeking fine-grained control and flexibility when building advanced AI agents that are tightly integrated with services in Google Cloud. It allows you to define agent behavior, orchestration, and tool use directly in code, enabling robust debugging, versioning, and deployment anywhere – from your laptop to the cloud.

---

## ✨ Key Features- **Code-First Development:** Define agents, tools, and orchestration logic for maximum control, testability, and versioning.
- **Multi-Agent Architecture:** Build modular and scalable applications by composing multiple specialized agents in flexible hierarchies.
- **Rich Tool Ecosystem:** Equip agents with diverse capabilities using pre-built tools, custom Python functions, API specifications, or integrating existing tools.
- **Flexible Orchestration:** Define workflows using built-in agents for predictable pipelines, or leverage LLM-driven dynamic routing for adaptive behavior.
- **Integrated Developer Experience:** Develop, test, and debug locally with a CLI and visual web UI.
- **Built-in Evaluation:** Measure agent performance by evaluating response quality and step-by-step execution trajectory.
- **Deployment Ready:** Containerize and deploy your agents anywhere – scale with Vertex AI Agent Engine, Cloud Run, or Docker.
- **Native Streaming Support:** Build real-time, interactive experiences with native support for bidirectional streaming (text and audio).
- **State, Memory & Artifacts:** Manage short-term conversational context, configure long-term memory, and handle file uploads/downloads.
- **Extensibility:** Customize agent behavior deeply with callbacks and easily integrate third-party tools and services.

## 🚀 InstallationYou can install the ADK using `pip`:

pip install google-adk

## 🏁 Getting StartedCreate your first agent (`my_agent/agent.py`):

\# my\_agent/agent.py
from google.adk.agents import Agent
from google.adk.tools import google\_search

root\_agent \= Agent(
    name\="search\_assistant",
    model\="gemini-2.0-flash-exp", \# Or your preferred Gemini model
    instruction\="You are a helpful assistant. Answer user questions using Google Search when needed.",
    description\="An assistant that can search the web.",
    tools\=\[google\_search\]
)

Create `my_agent/__init__.py`:

\# my\_agent/\_\_init\_\_.py
from . import agent

Run it via the CLI (from the directory *containing* `my_agent`):

adk run my\_agent

Or launch the Web UI from the folder that contains `my_agent` folder:

adk web

For a full step-by-step guide, check out the [quickstart](https://google.github.io/adk-docs/get-started/quickstart/) or [sample agents](https://github.com/google/adk-samples).

## 📚 ResourcesExplore the full documentation for detailed guides on building, evaluating, and deploying agents:

- **[Get Started](https://google.github.io/adk-docs/get-started/)**
- **[Browse Sample Agents](https://github.com/google/adk-samples)**
- **[Evaluate Agents](https://google.github.io/adk-docs/evaluate/)**
- **[Deploy Agents](https://google.github.io/adk-docs/deploy/)**
- **[API Reference](https://google.github.io/adk-docs/api-reference/)**

## 🤝 ContributingWe welcome contributions from the community! Whether it's bug reports, feature requests, documentation improvements, or code contributions, please see our [**Contributing Guidelines**](https://github.com/google/adk-python/blob/main/CONTRIBUTING.md) to get started.

## 📄 LicenseThis project is licensed under the Apache 2.0 License - see the [LICENSE](https://github.com/google/adk-python/blob/main/LICENSE) file for details.

---

*Happy Agent Building!*

