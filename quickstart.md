# Quickstart: Designing With Gemini Canvas + Cursor

> A guide for creating your first functional prototype with Gemini Canvas + Cursor

## TLDR;

- Start by using [Gemini Canvas](https://gemini.google.com/app) to rapidly prototype designs
- Export your Gemini projects to work with locally
- Use Cursor to set up a local development environment
- Iterate on your designs with Cursor Agent Mode
- Provide the right context to the agent, get end-to-end quickly, share safely and often

## Prerequisites

- Access to [Google Gemini]((https://gemini.google.com/app) 
- [Cursor](https://www.cursor.com/)
- [Git](https://formulae.brew.sh/formula/git) and some familiarity with coding workflows
- A [GitHub](https://github.com/) account (recommended)

## Phase 1: Rapid Prototyping with Gemini Canvas

1. **[Go to Google Gemini](https://gemini.google.com/app)** and describe what you want to build. Gemini will automatically switch to Canvas mode when you ask for UI/design elements. This is a good thing. This is where you will create design artifacts.
   - Ask it for something you actually want (avoid hypothetical design challenges)
   - Keep your requests simple and high-level initially
   - Use positive language ( "don't" or "avoid" tend to cause confusion )


3. **Iterate with Google Gemini Canvas** until you hit the point of diminishing returns.
   - **Gemini is great at zero-shot/one-shot prompting**, brainstorming, and laying in the broad strokes of a solution. 
   - **Know when to stop.** If Gemini starts making unwanted changes, or you start to require fine-grained changes, or if you want to share your project it's time to bring your project into your local environment and use Cursor.
   - **Ask Gemini how to run your project locally.** Before leaving Gemini request setup instructions for running your project locally and save them in the README file of your local project. 



## Phase 2: Use Cursor To Set Up A Local Dev Environment

Paste the instructions that Gemini created into the README file of your project and save it. 

Use `CMD+A` to select all the README text.

Use `CMD+L` to open the Cursor chat with selected text as context.

Use `CMD+I` to put Cursor into agent (aka YOLO) mode. 

Ask Cursor to help you set up the project and run it locally.

<img width="587" alt="image" src="https://github.com/user-attachments/assets/158e85f9-c35f-4240-a67b-0aa22d88d7d4" />  

  
The actual setup will vary from project to project but it's likely that Gemini has created some type of Node/React/TS application that will require you to install a bunch of depedencies. If you run into any errors while running commands, in the browser window, or wherever then paste the error text into the Cursor chat and Cursor will try and solve them. Most setup errors are trivial for the Cursor agent to fix.


## Phase 3: Iterate with Cursor

1. **Break down complex requests into smaller, focused tasks.** When working with Cursor, ask for one thing at a time for better results. For example, instead of asking Cursor to "Create a primary action button in the top right corner that triggers a modal asking users if they want to save, edit, or delete a text change, and if they choose delete, ask for confirmation." break it into separate requests:
   - "Create a primary action button in the top right corner"
   - "When the button is clicked, show a modal with save/edit/delete options"
   - "Add a confirmation dialog when the user selects delete"
   
   This approach makes it easier to identify and fix issues if something goes wrong.

2. **Work in tight iterations.** Make changes using Cursor chat, then test in your browser. Commit frequently with Git and share early for feedback. If Cursor makes a mistake or you want to undo a change, first try asking Cursor to revert it - this helps maintain context. If that doesn't work, use Git to revert the changes.

3. **Create a [product requirements](product-requirements.md) document or directory.** Store project-relevant information such as the problem statement, user personas, and roadmap. Keep it concise - too much information is just as bad as not enough. It can be valuable to prompt Cursor about its understanding of your product requirements and adjust accordingly.

4. **Create a [design path](design-path.md) document.** Document important design decisions and their rationale. This serves as a reference point when Cursor needs to "cool down" and be brought back up to speed. It also helps you recall why certain decisions were made. Design iterations with Cursor move quickly, and important context can be lost by the twentieth, thirtieth, or hundredth iteration. Additionally, this document helps others follow along when presenting your work.

5. **Ask Cursor to conduct a security review** before checking your code into a public repo ask Cursor if it is safe to do so. A common mistake is checking your API keys into a public repo. Cursor will discover issues like that.

6. **Post to GitHub and/or Create a demo video.** Share early and often. Collapsing the time it takes to create a prototype is less of a benefit if nobody has access to you are working on. The goal is to iterate quickly and learn. Ship a video of the end-to-end flow daily to somebody... anybody.


## Common Issues

**❓ Gemini gets confused or makes unwanted changes**
→ Start a new Canvas session or move to Cursor

**❓ Code doesn't work locally**
→ Paste the error into Cursor chat for a fix

**❓ Cursor seem "stuck"**
→ Start a fresh chat session or take a break
