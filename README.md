HEAD
<p align = "center" draggable=”false” ><img src="https://github.com/AI-Maker-Space/LLM-Dev-101/assets/37101144/d1343317-fa2f-41e1-8af1-1dbb18399719" 
     width="200px"
     height="auto"/>
</p>

## <h1 align="center" id="heading">Session 2: Embeddings and RAG</h1>

# Why We Created This New Repository

This repository is a clean version of my AI Engineering Boot Camp (Cohort 6) work. I needed to create this fresh repository for an important security reason.

## The Security Issue

During development of my RAG (Retrieval Augmented Generation) application, I accidentally included my OpenAI API key directly in the code. This happened in a configuration file:

```python
# The problematic code in the original repository
OPENAI_API_KEY = "sk-1234567890abcdefghijklmnopqrstuvwxyz"
```

When I tried to push my code to GitHub, their security scanning correctly blocked the push to protect my API key from being exposed publicly.

## Why a New Repository Was Necessary

Even after removing the API key from the current version of the code, GitHub continued to block the push. This happened because:

1. Git keeps a complete history of all changes
2. The API key was still present in the repository's history
3. GitHub scans the entire history, not just the latest version

## The Solution

To solve this issue, I:

1. Created a brand new repository
2. Copied all my files to a clean folder
3. Made sure to remove any API keys and use environment variables instead
4. Added proper `.gitignore` settings to prevent future issues
5. Initialized a fresh Git history without any sensitive information

This approach gave me a completely clean start without any sensitive information in the Git history.

## What I Learned

This experience taught me several important lessons about security and Git:

1. Never commit API keys or other secrets directly in code
2. Use environment variables for sensitive information
3. Add configuration files with secrets to `.gitignore`
4. Create template files (like `config.template.py`) that show the structure without real credentials
5. Check what you're committing with `git diff --staged` before each commit

## How I'm Handling API Keys Now

I've switched to using environment variables for all sensitive information:

```python
# The secure way to handle API keys
import os
OPENAI_API_KEY = os.getenv("OPENAI_API_KEY", "")
```

This keeps my API keys secure while still allowing the code to function properly.

## About This Project

This repository contains my work for the AI Engineering Boot Camp, including a RAG application that can process both text and PDF files to answer questions based on their content.

---

*Note: If you're working on a similar project, remember to set up your `.gitignore` file and environment variables before making your first commit!*


### [Quicklinks](https://github.com/AI-Maker-Space/AIE6/tree/main/00_AIM_Quicklinks)

| 🤓 Pre-work | 📰 Session Sheet | ⏺️ Recording     | 🖼️ Slides        | 👨‍💻 Repo         | 📝 Homework      | 📁 Feedback       |
|:-----------------|:-----------------|:-----------------|:-----------------|:-----------------|:-----------------|:-----------------|
| [Session 2: Pre-Work](https://www.notion.so/Session-2-Embeddings-Retrieval-Augmented-Generation-RAG-1c8cd547af3d81978a5af041c0d5b30a?pvs=4#1c8cd547af3d818daab3db56a5e631e9)| [Session 2: Embeddings, Retrieval Augmented Generation (RAG)](https://www.notion.so/Session-2-Embeddings-Retrieval-Augmented-Generation-RAG-1c8cd547af3d81978a5af041c0d5b30a) | [Recording](https://us02web.zoom.us/rec/share/gSn6QuqteVM4gYK9SslqMLx4MRVcwVj1S9RT-wJQYUuSVBkJ14-Fj8qY8d7Tyx-9.7ijgK2xRDpWFZ-bu) (lz2MTcF=)| [Session 2: Embeddings and RAG](https://www.canva.com/design/DAGjaSBtoao/n8G0T_O-2OIQHvgTfqyAxg/edit?utm_content=DAGjaSBtoao&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton) | You Are Here! | [Session 2 Assignment: Embeddings & RAG](https://forms.gle/FNkAuvdZe8eiaLTC8)| [AIE6 Feedback 4/3](https://forms.gle/iDTwhJ2nLp5CGkqP6)


### Outline:

🤜 BREAKOUT ROOM #1:
- Task 1: Imports and Utilities
- Task 2: Documents
- Task 3: Embeddings and Vectors
- Task 4: Prompts
- Task 5: Retrieval Augmented Generation
     - 🚧 ACTIVITY #1: Augment RAG

### Steps to Run:

1. Install UV - which you can do through [this resource](https://docs.astral.sh/uv/#getting-started)
2. Run the command `uv sync`
3. Open your Jupyter notebook and select `.venv` for your kernel. 

# Build 🏗️

Run the notebook!

# Ship 🚢

- Add one of the following "extras" to the RAG pipeline:
     - Allow it to work with PDF files
     - Implement a new distance metric
     - Add metadata support to the vector database
- Make a simple diagram of the RAG process
- Run the notebook
- Record a Loom walking through the notebook, the questions in the notebook, and your addition!

# Share 🚀
- Show your App in a loom video and explain the diagram
- Make a social media post about your final application and tag @AIMakerspace
- Share 3 lessons learned
- Share 3 lessons not learned

Here's a template to get your post started!

```
🚀 Exciting News! 🎉

I just built and shipped my very first Retrieval Augmented Generation QA Application using Chainlit and the OpenAI API! 🤖💼 

🔍 Three Key Takeaways:
1️⃣ The power of combining traditional search methods with state-of-the-art generative models is mind-blowing. 🧠✨
2️⃣ Collaboration and leveraging community resources like AI Makerspace can greatly accelerate the learning curve. 🌱📈
3️⃣ Dive deep, keep iterating, and never stop learning. Each project brings a new set of challenges and equally rewarding lessons. 🔄📚

A huge shoutout to the @AI Makerspace for their invaluable resources and guidance. 🙌

Looking forward to more AI-driven adventures! 🌟 Feel free to connect if you'd like to chat more about it! 🤝

#OpenAI #Chainlit #AIPowered #Innovation #TechJourney
```






# aie-clean
d022a4f1156ceca3436ccd54e28147c51ef9cc81
