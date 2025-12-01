# 🤖 Agent Builder: Task Automation Code Generator

This project utilizes the **Google Agent Development Kit (ADK)** to create a sophisticated, multi-agent system designed to take natural language task descriptions and generate executable automation code.

It effectively breaks down complex tasks, plans the execution steps, and finally generates the corresponding code to automate the desired workflow.

## ✨ Features

* **Natural Language Processing (NLP):** Accepts user prompts describing complex automation tasks (e.g., "Monitor my Gmail for emails from 'Acme Corp' and upload any attachments to my Google Drive folder named 'Invoices'").
* **Multi-Agent Architecture:** A pipeline of three specialized agents ensures robust planning and accurate code generation.
* **Google ADK Integration:** Built upon the powerful capabilities of the Google ADK for agent orchestration and reliable function calling.

## 🚀 Agent Architecture Overview

The system is composed of three interconnected agents, each with a distinct role in the code generation pipeline.



---

### 1. 📝 Task Breakdown Agent

**Role:** The initial agent responsible for receiving the user's high-level task description and converting it into a structured, granular list of sub-tasks and necessary inputs/outputs.

**Input:** User's natural language task prompt.
**Output:** A structured data format (e.g., JSON or list of strings) detailing the atomic steps required to complete the task.

### 2. 🗺️ Task Planner Agent

**Role:** Takes the structured sub-tasks from the Breakdown Agent and organizes them into an optimal, logical sequence of execution. It determines which external tools (Google services, APIs, etc.) are needed for each step and establishes the flow of data between them.

**Input:** Structured list of sub-tasks.
**Output:** A definitive execution plan or a 'workflow DAG (Directed Acyclic Graph)' that the Code Generator can follow, including tool/API references.

### 3. 💻 Code Generator Agent

**Role:** The final agent that writes the actual, runnable code based on the detailed plan provided by the Task Planner. It is specialized in generating code (e.g., Python, JavaScript) that interacts with the specified APIs (like Google Drive, Gmail, Calendar, etc.) to automate the task.

**Input:** Detailed execution plan/workflow from the Task Planner.
**Output:** A complete, well-commented code snippet or file that the user can execute.

---

## ⚙️ Prerequisites

To run this agent builder, you will need:

* **Google ADK CLI:** Installed and configured on your system.
