# Crebain AI 🐦‍⬛

**An AI-powered multi-agent research system that turns questions into structured, evidence-backed reports.**

Crebain AI is a research automation platform built with Python, LangChain, and LangGraph. It orchestrates specialized AI agents to search for relevant information, analyze findings, generate research reports, and evaluate report quality through an iterative feedback loop.

The goal is to make AI-assisted research more structured, transparent, and reliable by separating information gathering, analysis, writing, and quality evaluation into distinct stages.

## Features

- **Multi-Agent Research Workflow** — Coordinates specialized agents through a LangGraph workflow.
- **Automated Web Research** — Gathers relevant information to investigate a given research topic.
- **AI-Powered Analysis** — Organizes research findings into meaningful insights.
- **Structured Report Generation** — Produces coherent reports based on gathered evidence.
- **Iterative Quality Control** — Evaluates generated reports and routes them back for revision when necessary.
- **Modular Architecture** — Separates research, analysis, report generation, and quality evaluation into individual workflow nodes.

More capabilities, including persistent research history, document-based retrieval, report exports, and detailed workflow observability, may be added as development progresses.

## How It Works

Crebain AI uses a graph-based workflow to coordinate its research process.


flowchart TD
    START([Start]) --> SUP["Supervisor"]
    SUP --> SEARCH["Search Agent"]
    SEARCH --> ANALYST["Analyst"]
    ANALYST --> WRITER["Report Writer"]
    WRITER --> QC{"Quality Checker"}

    QC -->|Needs revision| WRITER
    QC -->|Passes quality checks| END([End])

    classDef process fill:#20242c,stroke:#737b8c,color:#f4f4f5,stroke-width:1.5px
    classDef decision fill:#342a49,stroke:#a78bfa,color:#f5f3ff,stroke-width:1.5px
    classDef terminal fill:#183b32,stroke:#4ade80,color:#f0fdf4,stroke-width:1.5px

    class SUP,SEARCH,ANALYST,WRITER process
    class QC decision
    class START,END terminal


The workflow follows these stages:

1. **Supervisor** — Coordinates the research workflow.
2. **Search Agent** — Retrieves information relevant to the research query.
3. **Analyst** — Processes and interprets the gathered findings.
4. **Report Writer** — Generates a structured research report.
5. **Quality Checker** — Evaluates the report and provides feedback for revision when necessary.

The final report is returned after the workflow satisfies its quality criteria.

## Tech Stack

The initial implementation is based on the following technologies:

- **Language:** Python
- **Agent Framework:** LangChain
- **Workflow Orchestration:** LangGraph
- **LLM Providers:** To be documented based on the configured providers
- **Web Search:** To be documented based on the selected search integration

The application stack may expand as the project develops into a full-stack application.

## Project Status

**Status: In development**

Features described as planned are not necessarily implemented yet.
