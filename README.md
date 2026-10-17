<b>Building software that asks better questions</b>

Most breakdowns in communication, between people and between people and AI, come from context nobody defined. I build tools that define it first, using the Socratic method.

10+ libraries on PyPI · two full applications · 1,300+ commits · Docker-ready

The idea

Someone in a room of smokers uses an empty glass as an ashtray. A non-smoker walks in and is asked to "pass the ashtray." They see glasses, no ashtray, and look confused. Same word, two contexts: for one it means a purpose-built object, for the other any container serving that function.

We assume context is shared when it often isn't. When context is an undefined variable, the same words mean different things, assumptions stay hidden, and misunderstandings surface late, when fixing them is expensive. The same thing happens when we describe a project to an AI: it builds exactly what we said, not what we meant.

Socrates' answer was don't tell, ask: declare you don't understand, ask for a definition, test it against exceptions, ask for a better one, repeat until both sides mean the same thing. I turn that loop into software.

<b>Two settings, one method:</b>

[Socrates](https://github.com/Nireus79/Socrates): human ↔ AI
A multi-agent platform that clarifies a project before anything is built. It asks structured questions across business context, constraints, requirements and priorities, extracts the answers into explicit context, flags conflicts (for example, real-time updates against a small budget), and tracks how mature that understanding is across discovery, analysis, design and implementation. When it's ready, it generates the specification.

Python, FastAPI, ChromaDB, PostgreSQL/SQLite, Docker; works with Claude, OpenAI, Google and Ollama
Status: v0.2.0, alpha testing

[Μώλυ (Moly)](https://github.com/Nireus79/Moly): human ↔ human
A communication coach that applies the same questioning before you send a message: what's missing from the context, how the other person sees it, and which assumptions you're making.

Go backend, local web interface and browser extension
Local-first: encrypted local database; runs fully offline with Ollama, or with Claude/OpenAI if you prefer
Detects crisis language and surfaces helplines (US/UK resources today, localization planned). Moly is a thinking aid, not a medical or crisis service.
Status: beta

Beyond questions: principles and systemic quality

Two further ideas run through the platform:

Principles enforced at runtime. Constitutional-style rules (privacy, budget, compliance, quality) are checked as agents act, so a shortcut that violates a principle is intercepted and an alternative is proposed. I also explore Socratic principles as a security framework.
No greedy optimization. A quality-control agent evaluates whole workflows end to end, so agents don't optimize one step at the expense of the system.
The libraries

Each piece is a standalone PyPI package, so you can use only what you need.

Library	What it does:

[socratic-nexus](https://pypi.org/project/socratic-nexus/)	One interface to Claude, OpenAI, Google and Ollama

[socratic-agents](https://pypi.org/project/socratic-agents/)	Specialized agents for dialogue, code, review and conflict detection

[socratic-morality](https://pypi.org/project/socratic-morality/)	Constitutional governance and compliance checks

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

Everything lives at [hermesoftware.wordpress.com.](https://hermesoftware.wordpress.com/)

Work with me

Available for small projects and code reviews:

Multi-agent prototypes and orchestration
LLM integration across Claude, OpenAI, Google and Ollama
Retrieval (RAG) pipelines
Docker deployment and API design

📧 Nireus79@proton.me · GitHub Sponsors · [PyPI](https://pypi.org/user/Nireus79/)

Code reviews, bug reports and pull requests are welcome.

Stack: Go · Python · FastAPI · React · TypeScript · LangChain · PostgreSQL · Redis · ChromaDB · SQLite · Docker
