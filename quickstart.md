# Quickstart: Designing With Cursor

### TLDR;

- Open the Cursor chat and ask it to help you do something you want to do.

### Prerequisites

- [Cursor](https://www.cursor.com/)
- [A basic development environment](/development-environment-setup.md) and some familiarity with coding workflows
- If you are creating a design using PatternFly then it's helpful to install the [PatternFly documentation MCP server](https://cursor.com/install-mcp?name=context7&config=eyJ1cmwiOiJodHRwczovL21jcC5jb250ZXh0Ny5jb20vbWNwIn0%3D).


### Setup your project

This step is sounds harder than it actually is. All you are doing is setting up some files and folders to keep your project organized and Cursor on point. Cursor assumes it is operating in a developement environment so having a project with that type of structure helps it build context.

1. Create a project folder
2. Navigate to your project folder and run `git init` to start version control
3. Create a **README.md** file and paste in the instructions that Gemini created for running your project locally.
4. Create a **product-requirements.md** file. This file should contain your project description. It is possible to get really fancy with this, but a good place to start is by pasting in the Jira story you are working on or the text from a prompt that worked really well for you in Gemini.
5. Create a **design_path.md** file serve as your design decision log. This helps maintain context between sessions, and can help you recover if the process comes off the rails.
6. Copy your code from Gemini into a local file.

Your project should look something like this:

<img width="389" alt="image" src="https://github.com/user-attachments/assets/962a22e1-e127-4d35-a20e-6ea3d8c653c0" />
<br/>

7. Open your README file in Cursor. Paste in your setup instructions if they are not already there.
8. Use `CMD+L` to open the Cursor chat and check that it is using the README as context.
9. Use `CMD+I` to put Cursor into Agent Mode.

![cursor-elements](https://github.com/user-attachments/assets/f5ab9aa3-7da3-42ee-aabd-8d29a97fe12b)
<br/>

10. Ask Cursor to help you set up the project and run it locally.

<img width="587" alt="image" src="https://github.com/user-attachments/assets/158e85f9-c35f-4240-a67b-0aa22d88d7d4" />
<br/>

  
The actual setup will vary from project to project but it's likely that Gemini has created some type of Node/React/TS application that will require you to install a bunch of dependencies. If you run into any errors while running commands, in the browser window, or wherever then paste the error text into the Cursor chat, and Cursor will try and solve them. Most setup errors are trivial for the Cursor agent to fix.


## Iterate with Cursor

Cursor Agent mode is very simple to use. Just ask it to make changes and if you don't like what it produces, then ask it to revert the change. That said, here are some things that have worked for me, especially when creating prototypes that contain multiple files, real data, and other complexities.

1. **Break down complex requests into smaller, focused tasks.** When working with Cursor, ask for one thing at a time for better results. For example, instead of asking Cursor to "Create a primary action button in the top right corner that triggers a modal asking users if they want to save, edit, or delete a text change, and if they choose to delete, ask for confirmation." break it into separate requests:
   - "Create a primary action button in the top right corner"
   - "When the button is clicked, show a modal with save/edit/delete options"
   - "Add a confirmation dialog when the user selects delete"
   
   This approach makes it easier to identify and fix issues if something goes wrong.

2. **Work in tight iterations.** Make changes using Cursor chat, then test in your browser. Commit frequently with Git and share early for feedback. If Cursor makes a mistake or you want to undo a change, first try asking Cursor to revert it - this helps maintain context. If that doesn't work, use Git to revert the changes.

3. **Keep your [product requirements](product-requirements.md) document concise and up to date.** Storing data such as user personas, and roadmap items is fine but you want to be sure they are on point. Too much information is just as bad as not enough. It can be valuable to periodically prompt Cursor about its understanding of your product requirements and adjust accordingly.

4. **Keep your [design path](design-path.md) document concise and up to date.** Document important design decisions and their rationale. This serves as a reference point when Cursor needs to "cool down" and be brought back up to speed. It also helps you recall why certain decisions were made. Design iterations with Cursor move quickly, and important context can be lost by the twentieth, thirtieth, or hundredth iteration. Additionally, this document helps others follow along when presenting your work.

5. **Ask Cursor to conduct a security review** before checking your code into a public repo ask Cursor if it is safe to do so. A common mistake is checking your API keys into a public repo. Cursor will discover issues like that.

6. **Share early and often.**  Cursor collapses the time it takes to create mockups and prototypes so you can focus on generating deep insights and continual feedback. Nobody can benefit from that unless you share what you are doing immediately. The goal is to iterate quickly and learn. Ideally you will be able to share a live deployment or your code on GitHub. Until you have that set up you should ship a video of the end-to-end flow daily to somebody... anybody.

## Next Steps

**Deploy your prototype to Vercel**  
Share your working prototype by deploying it to [Vercel](https://vercel.com/) for easy sharing and feedback.

**Share your code on GitHub**  
Upload your code to [GitHub](https://github.com/) for version control and collaboration.

**Get feedback and iterate**  
This is the whole point!

## Common Issues

**Gemini gets confused or makes unwanted changes**  
→ Start a new Canvas session or move to Cursor.

**Code doesn't work locally**  
→ Paste the error into Cursor chat for a fix. Most setup and runtime errors can be resolved by Cursor. Simply copy the error message from your terminal, browser console, or wherever it appears and paste it into the Cursor chat. Cursor excels at debugging and will often provide specific solutions or code fixes.

**People don't ask Cursor when they get stuck**  
→ Cursor is really good at solving issues. Don't hesitate to ask it for help.

**Cursor seems "unresponsive**  
→ Start a fresh chat session or take a break. If Cursor starts giving repetitive or unhelpful responses, or if it seems to have lost context, try starting a new chat session. Sometimes taking a short break and returning with a fresh perspective helps both you and Cursor get back on track.

**Git conflicts or version control issues**  
→ Ask Cursor to help resolve merge conflicts or explain Git commands. Cursor can walk you through resolving conflicts, understanding what went wrong, and getting your repository back to a clean state.

**Browser shows errors or blank page**  
→ Check the browser console for errors and paste them into Cursor. Common issues include missing environment variables, incorrect import paths, or runtime errors that Cursor can quickly identify and fix.

**Performance issues or slow loading**  
→ Cursor can help optimize your code. Whether it's slow build times, large bundle sizes, or runtime performance problems, Cursor can analyze your code and suggest optimizations, better dependencies, or configuration changes.


