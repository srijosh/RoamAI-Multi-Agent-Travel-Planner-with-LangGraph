# ✈️ RoamAI — A Multi-Agent Travel Planner with LangGraph

An AI travel planner that turns a natural-language trip request into a practical travel plan with flight suggestions, hotel ideas, and a day-by-day itinerary. The project uses a multi-agent workflow built with LangGraph, LangChain, and FastAPI.

The application is deployed on **Render** for public use, leveraging a cloud-hosted **PostgreSQL** database to persist user threads and conversation checkpoints across sessions.

Live Demo:

```text
https://roamai-multi-agent-travel-planner-with.onrender.com
```

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Tools and Technologies](#tools-and-technologies)

## Introduction

Planning a trip usually means jumping between multiple websites, tools, and spreadsheets. This project brings that flow into a single, unified experience. It uses an advanced multi-agent architecture coordinated through a LangGraph workflow to automate flight searches, hotel research, and itinerary generation.

By utilizing cloud infrastructure on **Render** tied to a **PostgreSQL** backend, the planner securely retains conversation states and user session checkpoints globally, ensuring your historical data isn't restricted to your local machine.
The system also integrates LangSmith for production-grade execution tracing, observability, and agent performance monitoring.

## Features

- **Multi-Agent Orchestration** via LangGraph to coordinate distinct, task-specialized AI agents such as flight agent, hotel agent, itinerary agent and final response agent.
- **Flight Research Integration** using live data fetches from the AviationStack API.
- **Hotel Suggestion Engine** utilizing Tavily search for real-time accommodation options.
- **Structured Travel Itineraries** providing clear, chronologically ordered day-by-day plans.
- **Clean Final Response Summary** providing clean summary with estimated budget and final recommendations.
- **Cloud Checkpointing & State Persistence** with PostgreSQL to handle multi-turn user threads seamlessly.
- **FastAPI Backend Architecture** coupled with a clean, dynamic web interface.
- **High-Performance Inference** driven by optimized Groq LLMs.
- **Advanced Observability & Tracing** integrated via LangSmith to monitor, debug, and optimize multi-agent workflow chains in real-time.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/srijosh/RoamAI-Multi-Agent-Travel-Planner-with-LangGraph.git
```

2. Navigate to the project directory:

```bash
cd RoamAI-Multi-Agent-Travel-Planner-with-LangGraph
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Set up environment variables by creating a `.env` file from `.env.sample`.

## Usage

Start the FastAPI application server locally:

```bash
python app.py
```

Once running, open your web browser and navigate to:

```text
http://127.0.0:8000/
```

## Tools and Technologies

- **LangGraph & LangChain**: Multi-agent workflow state management and tool-calling infrastructure.
- **FastAPI**: High-performance web framework for backend routing, serving asset mounts, and handling requests.
- **Standard HTML/CSS/JavaScript**: Vanilla frontend stack utilized to build, style, and handle interactive elements on the user interface.
- **Jinja2Templates**: Template engine implemented strictly within FastAPI to look up, load, and render the static UI templates.
- **PostgreSQL**: Cloud-ready database integration managing persistence for agentic checkpoints and user session history.
- **Groq**: Ultra-fast LLM serving engine utilized for prompt execution.
- **AviationStack API**: External travel integration providing flight telemetry and routing information.
- **Tavily API**: Search engine optimized for LLMs to scrape up-to-date hotel data.
- **LangSmith**: Developer platform used for production-grade tracing, debugging, and evaluating your multi-agent LangGraph workflows.
