# ✨ WishList ✨
A list of projects I already tackled of thinking about and might develop in the future! 🚀

## 🤖 MOE - Pruner
A way to fuse experts from a Mixture of Experts (MoE) models to reduce the total number of parameters. ✂️

Currently working on DeepSeek V2 Lite and DeepSeek V2 Lite Coder models.  Refining it to work on larger MoEs like DeepSeek V3 or the future Qwen 3 release.

🚧 WIP 🚧

[moe-pruner on GitHub](https://github.com/gabrielolympie/moe-pruner)

## 🧠 LLM - Pruner
A project similar to [moe-pruner](https://github.com/gabrielolympie/moe-pruner), but focused on dense Large Language Models (LLMs). 💡

Principles to leverage:
- **Low-Rank Decomposition:** Decompose linear layers from the MLP of an LLM into low-rank matrices for memory efficiency. Inference compute should remain similar. 📉
- **Successive Layer Fusions:** Fuse successive layers in an LLM to reduce the number of layers, improving both memory and compute efficiency. 🤝
- **Successive Layer Parallelism:**  Parallelize successive layers in an LLM for compute efficiency (akin to MoE decomposition). ⚡️

## 📝 Notion React Markdown
Creating a React component that mimics the Notion editor, but works with pure Markdown for better LLM interoperability. ✍️

Resources:
- [Milkdown](https://github.com/Milkdown/milkdown): A Markdown editor framework. 🥛
- [Crepe](https://milkdown.dev/docs/guide/using-crepe):  A Milkdown component. 🥞

Challenges:
- Achieving modularity and efficient backend interactions with the current implementation. 🧩

## 🦀 Python Rust Transpiler
A transpiler to generate Rust implementations of Python functions, with Python bindings for efficient integration. 🐍➡️🦀

Principles to leverage:
- Current Reinforcement Learning (RL) techniques for LLMs enable test-oriented self-improvement. 🧪
- Rust offers safety and performance guarantees, enhancing LLM robustness. 💪
- LLMs can generate Rust code from Python code. 🤖
- Unit tests and profiling will validate and optimize the transpiler. 📊

Challenges:
- Learning Rust! 😅

## 🚀 YoPo - You Only Prompt Once
Current LLM workflows often require complex frameworks (Haystack, LangChain, etc.) to create Directed Acyclic Graph (DAG) workflows, which can be tedious. 😩

YoPo aims to simplify this by allowing you to define a workflow with a single prompt, automatically generating the DAG with optimized parallelism. 🪄

[YoPo on GitHub](https://github.com/gabrielolympie/YoPo) (already quite powerful, but the formalism can be refined).

## 🌌 YoPo 2 - You Only Prompt Once 2
Building on YoPo, imagine defining a graph of agents, where each node is an LLM with specific tools, connected to other LLMs.  The LLM automatically processes input and decides where to send it. 🧠🔗🧠

YoPo 2 enables a simple way to define this agent graph and let it run autonomously until it reaches terminal endpoints. 🏁

[YoPo V2 on GitHub](https://github.com/gabrielolympie/YoPo_V2) (unfinished, but potentially revisited).

## ⚙️ Py3CL - 3CL Method in Python
A legacy project reproducing the 3CL method and providing tools to optimize a given Distributed Processing Engine (DPE). 🛠️

It's about 95% accurate and runs quickly (around 10k DPE/second on a single CPU core). Includes a basic Streamlit interface. 📈

Also implemented a constraint optimization method for DPE optimization (not publicly available yet, but can be provided upon request). 🎁

[Py3CL on GitHub](https://github.com/gabrielolympie/Py3CL)

## 🎨 VisualAIFlows - Python Backend for Rivet
I was searching for visual LLM workflow tools and was impressed by [Rivet](https://rivet.ironcladapp.com/) from IronClad. 🤩

The challenge was that it was in TypeScript, and I wasn't a full-stack developer at the time.

So, I created a basic Python backend (using FastAPI) to create simple Rivet graphs (based on HTTP nodes) that query the backend easily. 🐍

The backend automatically generates the necessary graphs to use new routes within Rivet, simplifying plugin implementation. 🔌

I paused this project when I realized that no-code tools aren't ideal for production environments, and the only ones I'd consider are those that allow code export. 📦

Still great for rapid prototyping and proof-of-concept work! ✨

[VisualAIFlows on GitHub](https://github.com/gabrielolympie/VisualAIFlows)