# ✨ WishList ✨
A curated list of projects I've tackled or am actively thinking about developing! 🚀 This is my playground for exploring exciting ideas in the world of AI and beyond.

## Highlights:
- Moe Pruner : Prune experts in MOE to create reasonably sized distilled models.
- Prompt Server : Turn any prompt in a fast api route
- Notion React Markdown :  it's notion, but it's also markdown, and it's llm friendly.
- Python rust transpiler : convert any python code into rust code with python bindings, with RL.
- Yopo: Parallel Dags workflows, from a single prompt.
- Yopo 2 : Any graph workflow, from a single prompt.
- Py3CL : 3Cl method for DPE calculation, in python.
- VisualAIFlows : Fastapi server for rivet.

🚧 **Work in progress** 🚧

### 🤖 MOE - Pruner
A project focused on intelligently fusing experts within Mixture of Experts (MoE) models to reduce the overall parameter count. ✂️ Think of it as slimming down powerful AI models without sacrificing too much performance!

Currently refining it for DeepSeek V2 Lite and DeepSeek V2 Lite Coder models. The goal is to scale this up to even larger MoEs like DeepSeek V3 or the upcoming Qwen 3 release. 

[🔗 GitHub Repo](https://github.com/gabrielolympie/moe-pruner)


### 📝 Notion React Markdown
Building a React component that replicates the familiar Notion editor experience, but with the flexibility of pure Markdown. ✍️ This will make it easier to integrate LLMs with a user-friendly editing interface.

Resources:

*   [🥛 Milkdown](https://github.com/Milkdown/milkdown): A fantastic Markdown editor framework.
*   [🥞 Crepe](https://milkdown.dev/docs/guide/using-crepe): A powerful Milkdown component.

Challenges:

*   🧩 Achieving a modular design and efficient backend integration.

Actually finished, I'll open source it some days.

### 🚀 Prompt Server
A FastAPI server that simply serves prompts, no code required.

## Why Prompt Server?
- Eliminates repetitive boilerplate code for prompt handling
- Enables rapid iteration by modifying prompts without code changes
- Standardizes prompt management across projects
- Simplifies integration with frontend applications

## Features
- **Prompt-first architecture**: Define prompts as markdown files - no additional code needed
- **Multi-provider support**: Works with any provider supported by [LiteLLM](https://docs.litellm.ai/docs/providers)
- **Multimodal capabilities**: Handle text, images, audio, video, and documents (varies by provider)
- **Streaming responses**: Get interleaved text and structured outputs
- **Automatic routing**: Prompt file paths become API endpoints automatically
- **Retry & fallback**: Built-in retry logic and fallback model support
- **Docker-ready**: Easy containerization for deployment

🚧 **FUTURE PROJECTS** 🚧

### 🧠 LLM - Pruner
Similar to [moe-pruner](https://github.com/gabrielolympie/moe-pruner), but this time targeting dense Large Language Models (LLMs). 💡 The aim is to make LLMs more efficient and accessible.

Key principles I'm exploring:

*   **📉 Low-Rank Decomposition:** Breaking down large linear layers into smaller, more manageable matrices to reduce memory usage, while maintaining inference speed. => tested, sounds good, doesn't works.
*   **🤝 Successive Layer Fusions:** Combining consecutive layers in an LLM to reduce the total number of layers, leading to both memory and computational savings. > tested with a naive implementation (layer merging without posttraining), doesn't work.
*   **⚡️ Successive Layer Parallelism:**  Parallelizing successive layers for faster processing, inspired by the decomposition techniques used in MoE models.


### 🦀 Python Rust Transpiler
A transpiler that automatically converts Python functions into optimized Rust code, complete with Python bindings for seamless integration. 🐍➡️🦀

The core ideas:

*   🧪 Leveraging Reinforcement Learning (RL) techniques to enable LLMs to self-improve through testing.
*   💪 Harnessing Rust's safety and performance guarantees to create more robust LLM applications.
*   🤖 Using LLMs to generate Rust code from Python, automating the translation process.
*   📊 Validating and optimizing the transpiler with thorough unit tests and profiling.

Challenges:

*   😅 Learning Rust (it's a journey!).

## Past / on hold Projects
### 🚀 YoPo - You Only Prompt Once
Tired of complex frameworks like Haystack or LangChain for building LLM workflows? 😩 YoPo simplifies things by letting you define an entire workflow with a *single* prompt. It then automatically generates a Directed Acyclic Graph (DAG) with optimized parallelism. 🪄

[🔗 GitHub Repo](https://github.com/gabrielolympie/YoPo) (already quite powerful, but always room for improvement!)

### 🌌 YoPo 2 - You Only Prompt Once 2
Taking YoPo to the next level! Imagine a graph of intelligent agents, each powered by an LLM with specific tools, connected and communicating with each other. 🧠🔗🧠

YoPo 2 makes it easy to define this agent graph and let it run autonomously until it reaches a desired outcome. 🏁

Key features:

*   **Triggers:** Conditions that determine when an agent should activate.
*   **Processes:** Actions performed by individual agents.
*   **Routers:** Mechanisms for agents to decide where to send their output.
*   **Terminal Nodes:** Points where the graph execution stops.

[🔗 GitHub Repo](https://github.com/gabrielolympie/YoPo_V2) (currently unfinished, but potentially being revisited!)

### ⚙️ Py3CL - 3CL Method in Python
A legacy project reproducing the 3CL method (a technique for distributed processing engine optimization) in Python. 🛠️

It's highly accurate (around 95%) and runs quickly (approximately 10,000 DPEs/second on a single CPU core). Includes a basic Streamlit interface for visualization. 📈

I've also implemented a constraint optimization method for DPE optimization (available upon request). 🎁

[🔗 GitHub Repo](https://github.com/gabrielolympie/Py3CL)

### 🎨 VisualAIFlows - Python Backend for Rivet
Inspired by the visual LLM workflow tool [Rivet](https://rivet.ironcladapp.com/) from IronClad. 🤩

I created a Python backend (using FastAPI) to generate simple Rivet graphs based on HTTP nodes, making it easier to query the backend. 🐍

The backend automatically generates the necessary graphs to integrate new routes within Rivet, streamlining plugin development. 🔌

I paused this project after realizing that no-code tools aren't always ideal for production, but it's still great for rapid prototyping! ✨

[🔗 GitHub Repo](https://github.com/gabrielolympie/VisualAIFlows)

---

## 🛠️ Tech Stack

My current toolkit for these projects:

*   **Languages:**
    *   Backend: Python (FastAPI, Pydantic, Pandas, NumPy, SciPy, Matplotlib, Seaborn, Scikit-learn, etc.)
    *   Frontend: Streamlit, React, Chakra UI, Gradio
    *   Database: Supabase, Meilisearch
*   **Specializations:**
    *   Deep Learning: PyTorch, TensorFlow, PyTorch Lightning
    *   LLM: Transformers, PEFT, Mirascope, ExLlama v2, VLLM
    *   Vector Databases: Meilisearch
    *   Optimization: Optuna, SciPy
    *   Parallelism: Numba, JobLib
    *   Data: Pandas, Datasets
    *   Visualization: Matplotlib, Seaborn, Plotly, Streamlit, Gradio
    *   Deployment: Docker, Fly
    *   Flow: Burr, Rivet
*   **Clouds:**
    *   Fly.io: 🥇 Best overall (simplicity, GPU cold start, feature-rich, but a bit pricey).
    *   GCP: ☁️ Most feature-rich, but expensive and GPU availability can be limited.
    *   RunPod: 🚀 Great for GPU availability; storage can be expensive (recommended for easy GPU notebook access).
    *   Scaleway: 🇫🇷 Best for data sovereignty and excellent features.
    *   Modal: ✨ Simplified deployments, great interface and features, but cold starts can be slow.
    *   Replicate: 📦 Exists!
*   **Tools / IDE:**
    *   VS Code
    *   Jupyter Notebook
    *   Continue.dev

---

## 🤝 Contributing

I welcome contributions to any of these projects!  Feel free to:

*   Open an issue to discuss a bug or feature request.
*   Submit a pull request with your changes.
*   Share your thoughts and ideas.

Let's build something amazing together! 🎉