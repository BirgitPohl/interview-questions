# ⚡️ Mini Chat App
We are very excited and congratulate you that you made it to the homework assigment step!
Now, we developers would like to get to know you better.
For this we have prepared this task and we hope you will enjoy it and find it exciting.

## Goal
You're building a lightweight agentic system that uses the Model Context Protocol (MCP) to orchestrate tools and execute multi-step tasks with minimal human input.

## Scope
Your mission is to build a small TypeScript application that:

1. Implements a simple agent ("TaskRunner") that:
  - Accepts high-level goals from the user (e.g., "Generate a weekly planning summary based on my notes").
  - Breaks the goal into actionable steps.
  - Calls MCP-based tools to execute those steps.
  - Produces a final, coherent output.
2. Integrates at least two MCP tools, for example:
- A file system tool (read/write local files).
- A search or API-fetch tool.
- A simple math or text transformation tool.
3. Runs a full “agent loop”:
- Reason about the next action
- Call the right MCP tool
- Store intermediate results
- Stop when the goal is completed
4. Exposes a CLI interface where someone can type:
- npm start (or npm run dev) "Summarize all .md files in ./notes and generate an action plan."

And the agent handles the rest.

## Quality bar
- Excellent code design.
- Linting + formatting (your stack’s standard).
- Sensible file structure and small functions.
- Type safety if available (TypeScript encouraged and preferred).
- One meaningful test.
- Example ideas: route rejects missing body, or reducer formats messages.
- Open up a CodeSanbox
- Use CodeSanbox and send us the link to your sandbox. Make sure that we can see the code and run the app.

## Scope Note
This sets up a minimal frontend/monolithical system. You can of course do more.
If you are not able to finish the scope: We still want to see what you have done.
In this case, we recommend that you stick to a part of the system, such as the UI,
or just the implementation to talk to the LLM or even smaller parts.
We want to see what you can do!

Write a note on what you would have done differently if you had more time!

## Questions
If you have any questions, don't hesitate to email us right away. We are happy to answer any.

The Homework follows a technical interview
After we have received your homework, we will meet for the technical interview where we focus on
- your communication skills
- and technical understanding

## Good luck and have fun!