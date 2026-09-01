# Day 1: Whitepaper Companion Podcast: Introduction to Agents and Vibe Coding
Source: https://www.kaggle.com/whitepaper-the-new-SDLC-with-vibe-coding

## Vibe coding vs. Agentic Engineering 
(Different in testing)  
Infinite trial and error vs. discrete, strict testing

## Context Engineering (core skill)
(need to balance 6 types of context) 

1. **Instruction**: define the agent’s core boundaries, which defines the agent’s core boundaries and persona
2. **Knowledge**: know about the environment the agent’s working in (e.g., architectural diagrams, API docs, style guides)
3. **Memory**: short-term session logs, long-term project state (know overarching goal and not lose the plot)
4. **Example**: reference patterns of good examples, so that it doesn’t have to invent a solution from scratch
5. **Tool**: exact APIs, CLIs, or file systems the agent is physically allowed to touch 
6. **Guardrail**: interceptors; catch the intent of dangerous paths, prevent, and block it before ever executing

⇒ Architectural decision (separate static context from dynamic context) 
- **Static context**: information that is always loaded into the AI’s brain for that project (core system file, like agents.md, that contains the unbreakable rules of the project) 
- **Dynamic context**: information loaded strictly on demand (build agent skills, give it a menu of skills) 

## The traditional SDLC shifts
- From weeks of development to hours
- Humans get moved to more of architecture and verification 
- Testing shifts, in the sense of not just for the code to compile, but more to evaluate the trajectory (checks the intermediate steps the AI took to arrive at its answer)

## Factory model
- Code is a byproduct 
- Primary output is the system that produces the code, the “factory”

## Anatomy of an agent
- Agent = model + harness
- The model only provides around 10% of the agent’s capability
- Harness: similar to scaffolding (should be well-engineered)  
(provides the transmission, steering wheel, and brake for the model)
  - Sandboxes: isolated environment where the AI can physically run and test the code without accidentally breaking the live production servers 
  - Orchestration logic: the brain that routes a massive task down to specialized sub-agents; observability infrastructure (logs, execution traces, cost metering) 

## Problems with agents
- Agent drift 
- Context rot

## Actual day-to-day life of a developer splits into two distinct modes of operation, depending on what they’re trying to build
1. Conductor mode: hands-on, real-time direction → highly interactive, keystroke to keystroke, immediate sub-second feedback (helpful for debugging or navigating through codebase that human intuition is still required for)
2. Orchestrator mode: asynchronous, high-level delegation → assign broad goals to background terminal agents (let the agent work independently in a sandbox and then review the pull request few hours later)

AI can create 80% of all features (the 80% problem); the final 20% is the weird edge cases, highly specific business logic, subtle system integrations that require deep human contextual knowledge that models simply do not possess yet

## CapEx & OpEx
AI flips the traditional software costs upside down: CapEx decreases, OpEX increases  
(instant gratification of a quick prototype vs. problems: interest payments, security flaws, technical debt, token burn, that will bankrupt the timeline later)
- Capital expenditure, CapEx: upfront cost to build 
- Operational expenditure, OpEx: ongoing cost to run and maintain the system 

Higher CapEx → financially sustainable, less work for OpEx, easier to deliver new features after first pass

Intelligent model routing (optimize OpEx even further)
- Route complex tasks to most robust models, while direct simple tasks (format JSON, text, etc.) to lightweight, simpler models

## Summary
- Shifting from wild west of casual vibe coding to strict, verifiable discipline of agentic engineering
- Code generation is a solved problem; physical typing of code is no longer the bottleneck
- The new craft of software engineering lies in context engineering, trajectory evaluation and harness design
- AI provides a powerful raw engine, but the human developer is entirely responsible for building the factory that contains it

## Codelabs
- Get started with Antigravity 2.0 and IDE  
https://codelabs.developers.google.com/getting-started-google-antigravity#0
- Build a Web Application in AI Studio and Deploy to Cloud Run
  https://codelabs.developers.google.com/deploy-from-aistudio-to-run?hl=en#0
