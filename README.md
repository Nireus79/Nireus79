<b>Building software that asks better questions</b>

Most breakdowns in communication, between people and between people and AI, come from context nobody defined. I build tools that define it first, using the Socratic method.

Free, private, open-source tools. Everything is listed at [nireus79.github.io](https://nireus79.github.io/).

The idea

Someone in a room of smokers uses an empty glass as an ashtray. A non-smoker walks in and is asked to "pass the ashtray." They see glasses, no ashtray, and look confused. Same word, two contexts: for one it means a purpose-built object, for the other any container serving that function.

We assume context is shared when it often isn't. When context is an undefined variable, the same words mean different things, assumptions stay hidden, and misunderstandings surface late, when fixing them is expensive. The same thing happens when we describe a project to an AI: it builds exactly what we said, not what we meant.

Socrates' answer was don't tell, ask: declare you don't understand, ask for a definition, test it against exceptions, ask for a better one, repeat until both sides mean the same thing. I turn that loop into software.

<b>Two products, one method:</b>

[Μώλυ (Moly)](https://nireus79.github.io/Moly/): human ↔ human
A communication coach that applies the same questioning before you send a message: what's missing from the context, how the other person sees it, and which assumptions you're making. It never decides for you.

Browser extension (Chrome and Chromium browsers, Firefox) plus a small app on your computer; an Android beta exists
Local-first: encrypted local database; runs fully offline with Ollama, or with your own Claude/OpenAI key
Free, open source (MIT). Moly is a thinking aid, not a medical, legal or crisis service.
Status: beta

[Socrates](https://github.com/Nireus79/Socrates-ai): a conversation with artificial Greek philosophers
Socrates, Diogenes, Plato and Aristotle, each revived in today's world and speaking as himself. They ask hard questions, do not give verdicts, and remember what you told them, in your own words, which you can see and delete.

Runs on your own AI provider key, no server of ours; desktop and Android
Free, open source (MIT)
Status: early build, not released yet

Research: [Socrates (proof of concept)](https://github.com/Nireus79/Socrates) is the earlier Python multi-agent platform that clarifies a project before anything is built. It is not maintained as a product.

Two further ideas, explored in the libraries and the research prototype

Rules checked while agents act. Principles such as privacy, budget and quality are written as rules and checked at each step, so a shortcut that breaks one is stopped and an alternative is proposed. I also explore Socratic principles as a security framework.
No greedy optimization. A quality-control agent looks at a whole workflow, so agents do not optimize one step at the expense of the system.
The libraries

Each is a separate PyPI package. They are in early development; the research prototype that uses them is not maintained as a product.

Library	What it does:

[socratic-nexus](https://pypi.org/project/socratic-nexus/)	One interface to Claude, OpenAI, Google and Ollama

[socratic-agents](https://pypi.org/project/socratic-agents/)	Agents for dialogue, code, review and conflict detection

[socratic-morality](https://pypi.org/project/socratic-morality/)	Rules for agent behaviour, checked at runtime

[socratic-knowledge](https://pypi.org/project/socratic-knowledge/)	Knowledge management and semantic retrieval (RAG)

[socratic-workflow](https://pypi.org/project/socratic-workflow/)	Sequential, parallel and branching workflows

[socratic-conflict](https://pypi.org/project/socratic-conflict/)	Conflict detection and Socratic resolution

[socratic-maturity](https://pypi.org/project/socratic-maturity/)	Maturity tracking across project phases

[socratic-learning](https://pypi.org/project/socratic-learning/)	Learning loops for agents

[socratic-analyzer](https://pypi.org/project/socratic-analyzer/)	Code and quality analysis

[socratic-performance](https://pypi.org/project/socratic-performance/)	Monitoring and caching

[socratic-docs](https://pypi.org/project/socratic-docs/)	Documentation generation

What I'm investigating
Does asking clarifying questions before generation reduce specification errors and rework compared with one-shot prompting?
Can principle-based checks serve as a practical security and governance layer for AI agents?
How do you keep AI agents from greedy shortcuts that corrupt a system over time?

Read more
Solving the context problem that breaks human-AI communication
Constitutional AI as a security framework
Why greedy algorithms corrupt systems, and how to fix them
Conflict resolution between AI agents

Articles and background: [hermesoftware.wordpress.com](https://hermesoftware.wordpress.com/). Products and downloads: [nireus79.github.io](https://nireus79.github.io/).

How I work

I am an independent programmer in Greece. I build with AI coding assistants (Claude Code). I design the products, review the code and test it.

Work with me

Available for small projects and code reviews:

Multi-agent prototypes and orchestration
LLM integration across Claude, OpenAI, Google and Ollama
Retrieval (RAG) pipelines
Docker deployment and API design

📧 Hermes_creative@proton.me · [GitHub Sponsors](https://github.com/sponsors/Nireus79) · [PyPI](https://pypi.org/user/Nireus79/)

Code reviews, bug reports and pull requests are welcome.

Stack: Go · Python · FastAPI · React · TypeScript · LangChain · PostgreSQL · Redis · ChromaDB · SQLite · Docker
