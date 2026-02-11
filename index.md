---
layout: default
title: The Human Orchestrator
description: How I Built AAA Software with Manual AI Development
---

# The Human Orchestrator: How I Built AAA Software with Manual AI Development

**By [Stinger05189]**

Most people today are rushing toward "agentic" coders—autonomous frameworks like Google Anti-Gravity that promise to build software *for* you. They want a "set it and forget it" solution. But after spending thousands of hours coding with AI over the last year, I’ve found that the real power isn't in letting the AI be the captain. It’s in becoming a **Human Orchestrator**.

I am writing this not to sell you a tool, but to show you what is possible. I have no traditional coding background. Just a year ago, my experience was limited to Unreal Engine Blueprints. Today, I am building complex C++ plugins, custom ECS systems, and full-stack web applications that rival professional studios.

And I did it by doing the opposite of what the industry suggests: I rejected the agents and embraced a manual, high-control workflow using **Google AI Studio** and **Gemini 3.0 Pro**.

Here is why—and exactly how—I do it.

---

## The Case Against "Auto-Pilot"

There is a prevalent belief that tools like Google Anti-Gravity are the endgame. While impressive, I’ve found that relying on agentic frameworks introduces friction that actually slows down high-quality development:

* **Loss of "Taste":** An agent doesn't know your architectural vision or your personal style. It solves the problem, but often in a way that feels generic or disjointed.
* **The "Death by 1,000 Cuts":** Agents often introduce small errors—truncated lines for brevity, minor syntax diffs, or changes to unrelated code. These require constant debugging that breaks your flow.
* **Context Inefficiency:** Agents often struggle to know *which* files to load. They might miss a crucial header file or waste tokens reading irrelevant ones.
* **Cost:** The constant planning, tool calling, and iterating of an agent burns through quota and credits rapidly.

By switching to a manual chat interface (Google AI Studio), I remain the **gatekeeper**. I control every single line of code. This prevents the "drift" that happens with agents and ensures that the final codebase reflects *my* standards, not just the model's training data.

## My "Manual" Workflow

My process relies on treating Gemini not as a worker bee, but as a high-level partner that I guide with extreme precision. Here are the pillars of my workflow.

### 1. The Context Manager
I don't just drag-and-drop files. I use a custom-built context management tool that generates a **Markdown File Tree** of my entire project.
* Even if a file isn't loaded into the context window, Gemini can see the file tree. It understands the project structure, where things live, and how they relate.
* I create "Context Presets" for different tasks (e.g., "Audio System," "UI Framework") to instantly load only the relevant files.
* With Gemini 3.0 Pro Preview, I comfortably use 100k+ tokens for development and up to 200k+ for deep research or review.

### 2. The "Gemini Directory"
In the root of every project, I keep a directory specifically *for* the AI. It contains:
* **Role Definitions:** Explaining Gemini's specific role in this project.
* **Protocols:** Standard operating procedures for how we write code.
* **The Dev Log:** A running memory of what we’ve achieved, decisions made, and technical debt to address.
* **Learnings:** A file where Gemini records "lessons" about the codebase so it doesn't repeat mistakes.

### 3. The "Diff" Protocol
This is the secret sauce. I rarely ask Gemini to rewrite a whole file. I instruct it to provide **optimally formatted diffs**.
* It skips unchanged code (e.g., `// ... void SomeFunction(){} ... existing code ...`).
* It provides changes in a format that my VS Code "Compare and Merge" tool can ingest perfectly.
* **The Result:** Gemini "learns" to focus its attention mechanism only on the *changes*, not the memory of the file. This allows us to operate on massive files without needing the full content in the context window every time.

### 4. Documentation First (The "Second Brain")
I never start coding a feature until it exists as documentation.
* I start in **Obsidian**, rambling and talking to my notes as if I’m talking to Gemini. I ask questions, outline logic, and "rubber duck" my ideas.
* I hand these raw notes to Gemini to restructure into formal documentation.
* This documentation is then stored in the project and fed back to Gemini during coding sessions.
* **Why this works:** A 30k token directory of documentation is worth years of experience. It grounds the AI in *truth* rather than *guesswork*.

---

## The "Greenlight" Session

I treat every coding session like a surgical operation. I don't just start chatting; I follow a strict loop:

1.  **Initialization:** I paste a specialized prompt that loads the "Gemini Directory" and the specific user request for the day.
2.  **The Plan:** Gemini proposes a detailed implementation plan for the session.
3.  **The `GREENLIGHT`:** I do not allow code generation until I type `GREENLIGHT`. This signals that I agree with the plan and we are ready to move.
4.  **The Loop:** We execute step-by-step. I manually implement the code, compile, and test. If there are errors, I paste them back.
5.  **Wrap Up:** At the end of the session, I command a "Wrap Up." Gemini updates the Dev Log and the Documentation to reflect the new state of the project.

---

## What Is Possible?

You might think this manual process sounds slow. It is not. It is a multiplier.

In the last year, I have built:
* **Momentum UI Plugin:** A massive Unreal Engine plugin with over **16k lines of C++** (20k+ with comments).
* **Documentation Engine:** A custom website (5k lines of TS/JS/HTML) that parses my C++ code and generates interactive API docs with node previews.
* **Custom Game Engine Architecture:** An Unreal Engine game featuring a custom Light ECS (Entity Component System) that allows for massive scale and performance—something I never could have touched with Blueprints alone.

Unreal Engine C++ is notoriously difficult. But because the engine's source code is public (a quarter-billion tokens of training data), Gemini understands it natively. When you combine that deep knowledge with a human orchestrator who manages the context and "taste," the result is professional-grade engineering from a non-coder.

## Conclusion

We are in a golden age of creation. You do not need to wait for an autonomous agent to build your dream project. In fact, you shouldn't.

By taking control, treating documentation as your foundation, and orchestrating the AI manually, you can build things that were impossible for a single person just two years ago. The AI is the engine, but you must remain the driver.
