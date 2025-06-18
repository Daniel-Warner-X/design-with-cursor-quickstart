# Quickstart: Designing With Gemini Canvas + Cursor

> A guide for creating your first functional prototype with Gemini Canvas + Cursor

## TLDR;

- Start by using Google Gemini Canvas to rapidly prototype designs
- Export your Gemini projects to work with locally
- Set up a local development environment with Cursor
- Iterate on your designs with Cursor Agent Mode
- Protips for AI-assisted design workflows

## Prerequisites

- Access to Google Gemini
- Cursor
- Git and some familiarity with coding workflows
- A GitHub account (recommended)

## Phase 1: Rapid Prototyping with Gemini Canvas

1. **[Go to Google Gemini](https://gemini.google.com/app)** and describe what you want to build. Gemini will automatically switch to Canvas mode when you ask for UI/design elements. This is a good thing. This is where you will create design artifacts. Use these prompting strategies for best results:
   - Ask it for something you actually want (avoid hypothetical design challenges)
   - Keep your requests simple and high-level initially
   - Use positive language ( "don't" or "avoid" tend to cause confusion )


2. **Iterate with Google Gemini Canvas** until you hit the point of diminishing returns.
   - **Gemini is great at zero-shot/one-shot prompting**, brainstorming, and laying in the broad strokes of a solution. 
   - **Know when to stop**: When Gemini starts making unwanted changes, when you start to require fine-grained changes, or if you want to share your project it's time to bring your project into your local environment and use Cursor.
   - **Ask Gemini how to run your project locally** Before leaving Gemini request setup instructions for running your project locally and save them in the README file of your local project. 



## Phase 2: Use Cursor To Set Up A Local Dev Environment

### Step 4: Set Up Your Local Environment

Paste the instructions that Gemini created into the README file of your project and save it. 

Use `CMD+A` to select all the README text.

Use `CMD+L` to open the Cursor chat with selected text as context.

Use `CMD+I` to put Cursor into agent (aka YOLO) mode. 

Ask Cursor to help you set up the project and run it locally.

The actual setup will vary from project to project but it's likely that Gemini has created some type of Node/React/TS Applicaion that will require you to install a bunch of npm depedencies. If you run into any errors running commands, in the browser window, wherever then paste paste them into the Cursor chat and Cursor will try and solve them. Most setup errors are trivial for the Cursor agent to fix.


## Phase 3: AI-Powered Iteration with Cursor

### Step 7: Open in Cursor

1. **Open your project folder in Cursor**
2. **Create a `README.md`** with your project description
3. **Set up version control:**
```bash
git init
git add .
git commit -m "Initial project setup from Gemini"
```

### Step 8: Enhance Your Project

**Use Cursor Chat to:**
- Fix errors by pasting error messages directly into chat
- Ask for specific feature additions
- Request code improvements
- Debug issues as they arise

**Pro tip:** Ask for one thing at a time for better results.

---

## Phase 4: Project Organization & Best Practices

### Step 9: Organize Your Project

Create a `PRD/` directory with:
- **`problem-statement.md`** - What you're solving
- **`design-path.md`** - Key design decisions and milestones
- **`user-personas.md`** - Who you're designing for

### Step 10: Follow the Iteration Cycle

1. **Make changes** using Cursor chat
2. **Test immediately** in your browser
3. **Commit frequently** with Git
4. **Share early** for feedback

---

## Quick Reference: Best Practices

### ✅ Do This
- **Ask for one thing at a time** when working with AI
- **Get end-to-end functionality quickly** before polishing
- **Use real data** when possible for more realistic prototypes
- **Commit changes frequently** with descriptive messages
- **Share work early** with videos or demos

### ❌ Avoid This
- **Waterfall planning** - Don't over-specify upfront
- **Perfect-first mentality** - Iterate don't perfect
- **Working in isolation** - Share for feedback regularly
- **Ignoring errors** - Fix issues as they appear

---

## Troubleshooting

### Common Issues

**❓ Gemini gets confused or makes unwanted changes**
→ Start a new Canvas session or move to Cursor

**❓ Code doesn't work locally**
→ Paste the error into Cursor chat for instant fixes

**❓ AI tools seem "stuck"**
→ Start a fresh chat session or take a break

**❓ Project feels overwhelming**
→ Focus on one small feature at a time

---

## What's Next?

Once you have a working prototype:

1. **Conduct a security review** (if handling sensitive data)
2. **Post to GitHub** for collaboration
3. **Create a demo video** to share with stakeholders
4. **Gather feedback** and iterate

Remember: The goal is to iterate quickly and learn. GenAI design isn't always faster than traditional methods, but it enables deeper exploration of the problem space and delivers richer understanding of your design.

---

## Resources

- [Node.js Downloads](https://nodejs.org)
- [Cursor.ai](https://cursor.ai)
- [Google Gemini](https://gemini.google.com)
- [Vite Documentation](https://vitejs.dev)

---

## Appendix: Detailed Setup Instructions

<details>
<summary>Click here for detailed React + Tailwind setup instructions</summary>

### Detailed React Project Setup

If you need more detailed setup instructions, here's the complete process:

#### 1. Create React Project with Vite
```bash
npm create vite@latest my-notebook-reviewer -- --template react
cd my-notebook-reviewer
npm install
```

#### 2. Install and Configure Tailwind CSS v4
```bash
# Remove old Tailwind packages if they exist
npm uninstall tailwindcss postcss autoprefixer

# Install Tailwind v4
npm install -D tailwindcss@next
npm install -D @tailwindcss/typography
```

#### 3. Configure Tailwind

Create `postcss.config.js`:
```javascript
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```

Create `tailwind.config.mjs`:
```javascript
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [
    require('@tailwindcss/typography'),
  ],
}
```

#### 4. Add Tailwind to CSS

Update `src/index.css`:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

#### 5. Install Additional Dependencies

```bash
# If using Markdown
npm install marked

# Start development server
npm run dev
```

</details>


