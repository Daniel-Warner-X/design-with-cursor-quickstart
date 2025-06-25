# Jumpstart Your Project

There are several great options for getting from 0 to 1 with application builders like [Replit](https://replit.com/~) and [loveable.dev](https://lovable.dev/). For the sake of this example, I will be using [Google Gemini Canvas](https://gemini.google.com/app) because that is what we have access to at Red Hat. **Gemini excels at executing against zero-shot and one-shot prompts**, brainstorming, and laying out the broad strokes of a solution.

These tools are chat-based and easy to experiment with so just open up the chat and start typing.

There is no need to exhaustively specify what you want. However, there are a few guidelines that can help speed things up and get the results you want.

## Step-by-Step

### 1. Pick the right project

Hypothetical design problems are okay, but working on a real-world design task is the fastest route to actually getting value from these tools. You may even want to consider simply pasting the text from a Jira ticket.

### 2. **[Go to Google Gemini](https://gemini.google.com/app)**

### 3. **Prime the conversation** 

Put Gemini into the correct frame of mind by checking some of your assumptions. For example, I am creating a new card for the RHOAI Dashboard, so I check to make sure that Gemini is aware of the design system I am working with.

#### Example

**Prompt**

<img width="376" alt="image" src="https://github.com/user-attachments/assets/81e73263-a571-43f5-b420-1c018441d35c" />

**Response**

<img width="791" alt="image" src="https://github.com/user-attachments/assets/75699919-2a19-40d1-9c80-fba8b3dceda3" />

### 4. **Prompt**

Describe what you want to build. Gemini will automatically switch to Canvas mode when you ask for UI/design elements. **Keep your requests simple** and high-level initially. At this stage, too much information is worse than too little.

For example, this prompt has two primary requests. The first is for a design asset, the second is for the chat to ask clarifying questions. The second request got weighted more heavily causing confusion in the response.

Prompt

<img width="540" alt="image" src="https://github.com/user-attachments/assets/95b2346b-2e8d-4dd4-8a39-4e3226a7ba9b" />

Response

<img width="867" alt="image" src="https://github.com/user-attachments/assets/d4d71d58-58b0-41a0-a377-64ab287cd86c" />

Removing the second request improves the response.

Prompt

<img width="543" alt="image" src="https://github.com/user-attachments/assets/01653212-f309-4d7f-85fd-bd3165d885d0" />

Response

<img width="1427" alt="image" src="https://github.com/user-attachments/assets/7e1feb10-aa8f-447f-a375-976fd03c0772" />  


### 5. **Refine**

Iterate and improve your design.

#### Example

Prompt
<img width="523" alt="image" src="https://github.com/user-attachments/assets/8aabbbd2-6f86-4084-a987-1a380a4cb787" />
Response
<img width="561" alt="image" src="https://github.com/user-attachments/assets/f90f0f50-268f-446f-8d42-81b12fddeb9b" />

Prompt
Response
<img width="557" alt="image" src="https://github.com/user-attachments/assets/5f39b186-85e4-4404-a0e6-04255f35720d" />


### 6. **Know when to quit**

Recognize the point of diminishing returns. If Gemini starts making unwanted changes, or you start to require fine-grained changes, or if you want to share your project, it's time to bring your project into your local environment and use Cursor.

For example, Gemini started struggling when I started making refactor requests.

Prompt:

<img width="392" alt="image" src="https://github.com/user-attachments/assets/da11bdfd-e647-45c8-90c0-c3d219f73d7e" />

Result:

<img width="628" alt="image" src="https://github.com/user-attachments/assets/5c238523-a0e9-42dc-8a9e-0a9d21e3099c" />


### 7. **Go local**

Transition to your development environment. **Ask Gemini how to run your project locally** before leaving the platform. Request setup instructions for running your project locally and save them in the README file of your local project.


