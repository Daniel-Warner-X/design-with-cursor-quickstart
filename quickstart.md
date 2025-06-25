# Quickstart: Designing With Cursor

## TLDR;

- Open the Cursor chat and ask it to help you do something you want to do.

## Prerequisites

- [Cursor](https://www.cursor.com/)
- [A basic development environment](/development-environment-setup.md) and some familiarity with coding workflows
- If you are creating a design using PatternFly then it's helpful to install the [PatternFly documentation MCP server](https://cursor.com/install-mcp?name=context7&config=eyJ1cmwiOiJodHRwczovL21jcC5jb250ZXh0Ny5jb20vbWNwIn0%3D).

---

### 1. Setup your project

- **Create a project folder**
- **Initialize that folder as a Git repository**: Navigate to your project folder and run `git init` to start version control
- **Create a README.md file**: Create a README file and paste in the instructions that Gemini created for running your project locally.
- **Create a prd.md (Product Requirements Document) file**: This file should contain your project description, goals, and requirements. You can paste in your original prompt, text from a Jira story, user stories, or any other project specifications
- **Create a design_path.md file**: This file will serve as your design decision log. Use it to document milestone decisions, design rationale, and key choices you make throughout the development process. This helps maintain context between sessions.
- **Copy your code from Gemini into a local file**

  Your project should look something like this:

<img width="550" alt="image" src="https://github.com/user-attachments/assets/097f3766-4ca8-4494-90eb-bc1ac2a5a285" />

- Open your README file in Cursor. Paste in your setup instructions if they are not already there.
- Use `CMD+L` to open the Cursor chat and check that it is using the README as context.
- Use `CMD+I` to put Cursor into agent mode.

![cursor-elements](https://github.com/user-attachments/assets/f5ab9aa3-7da3-42ee-aabd-8d29a97fe12b)

- Ask Cursor to help you set up the project and run it locally.

<img width="587" alt="image" src="https://github.com/user-attachments/assets/158e85f9-c35f-4240-a67b-0aa22d88d7d4" />  

  
The actual setup will vary from project to project but it's likely that Gemini has created some type of Node/React/TS application that will require you to install a bunch of dependencies. If you run into any errors while running commands, in the browser window, or wherever then paste the error text into the Cursor chat, and Cursor will try and solve them. Most setup errors are trivial for the Cursor agent to fix.


## Phase 3: Iterate with Cursor

1. **Break down complex requests into smaller, focused tasks.** When working with Cursor, ask for one thing at a time for better results. For example, instead of asking Cursor to "Create a primary action button in the top right corner that triggers a modal asking users if they want to save, edit, or delete a text change, and if they choose to delete, ask for confirmation." break it into separate requests:
   - "Create a primary action button in the top right corner"
   - "When the button is clicked, show a modal with save/edit/delete options"
   - "Add a confirmation dialog when the user selects delete"
   
   This approach makes it easier to identify and fix issues if something goes wrong.

2. **Work in tight iterations.** Make changes using Cursor chat, then test in your browser. Commit frequently with Git and share early for feedback. If Cursor makes a mistake or you want to undo a change, first try asking Cursor to revert it - this helps maintain context. If that doesn't work, use Git to revert the changes.

3. **Create a [product requirements](product-requirements.md) document or directory.** Store project-relevant information such as the problem statement, user personas, and roadmap. Keep it concise - too much information is just as bad as not enough. It can be valuable to prompt Cursor about its understanding of your product requirements and adjust accordingly.

4. **Create a [design path](design-path.md) document.** Document important design decisions and their rationale. This serves as a reference point when Cursor needs to "cool down" and be brought back up to speed. It also helps you recall why certain decisions were made. Design iterations with Cursor move quickly, and important context can be lost by the twentieth, thirtieth, or hundredth iteration. Additionally, this document helps others follow along when presenting your work.

5. **Ask Cursor to conduct a security review** before checking your code into a public repo ask Cursor if it is safe to do so. A common mistake is checking your API keys into a public repo. Cursor will discover issues like that.

6. **Post to GitHub and/or Create a demo video.** Share early and often. Collapsing the time it takes to create a prototype is less of a benefit if nobody has access to what you are working on. The goal is to iterate quickly and learn. Ship a video of the end-to-end flow daily to somebody... anybody.


## Common Issues

**❓ Gemini gets confused or makes unwanted changes**
→ Start a new Canvas session or move to Cursor

**❓ Code doesn't work locally**
→ Paste the error into Cursor chat for a fix

**❓ Cursor seems "stuck"**
→ Start a fresh chat session or take a break
