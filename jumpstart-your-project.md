# Jumpstart Your Project with a Natural Language Application Builder

There are several great options for getting from 0 to 1 with application builders like Replit, loveable.dev, and GPT Canvas. For the sake of this example, I will be using Google Gemini because that is what we have access to at Red Hat. **Gemini excels at zero-shot/one-shot prompting**, brainstorming, and laying out the broad strokes of a solution.

These tools are chat-based and easy to experiment with and use. However, there are a few guidelines that can help speed up getting the results you want.

## Step-by-step

### 1. **[Go to Google Gemini](https://gemini.google.com/app)**

### 2. **Prime the conversation** 

Put Gemini into the correct frame of mind by checking some of your assumptions. For example, I am creating a new card for the RHOAI Dashboard, so I check to make sure that Gemini is aware of the design system I am working with.

**Prompt**

```
    Are you aware of Patternfly and it's dashboard pattern?
```
**Response**

```
Yes, I am aware of PatternFly and its dashboard pattern. PatternFly is an open-source design system maintained by Red Hat. It provides a set of guidelines, components, and patterns to help teams build consistent and scalable enterprise products. It's built to promote design commonality and improve user experience across various IT applications. PatternFly offers implementations in HTML/CSS, React, and Web Components (PatternFly Elements). The dashboard pattern in PatternFly is a common and crucial use case for enterprise applications...
```

### 3. **Prompt**

Describe what you want to build. Gemini will automatically switch to Canvas mode when you ask for UI/design elements. This is a good thing—this is where you will create design artifacts.

Keep your requests simple and high-level initially. At this stage too much information is worse than too little.


### 4. **Refine**

Iterate and improve your design

### 5. **Know when to quit**

Recognize the point of diminishing returns. If Gemini starts making unwanted changes, or you start to require fine-grained changes, or if you want to share your project, it's time to bring your project into your local environment and use Cursor

### 6. **Go local**

Transition to your development environment. **Ask Gemini how to run your project locally** before leaving the platform. Request setup instructions for running your project locally and save them in the README file of your local project.


