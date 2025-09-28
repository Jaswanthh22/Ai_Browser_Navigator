# Web Navigator AI Agent
## An autonomous AI agent that understands natural language and drives the web automatically.
This system combines a **locally running LLM** (for instruction understanding and planning) with a **browser automation setup** (Playwright/Selenium/Puppeteer) to execute user commands.

## Reason for taking this problem statement:
The growing difficulties for users encounter when navigating the complicated digital space is the main reason for choosing the problem statement **Web Navigator AI**. Traditional search engines frequently fail to deliver organized, context-aware, and useful information because of the billions of web pages, the variety of data formats, and the irrelevant of search results.These gaps are filled by an Web Navigator AI that:-
- Allow user to interact with browser with natural language,
- Perform browsing ,filtering,scraping and structuring data without manual effort,
- Give results in a structured format such as summaries and comparisons.

The AI Web Navigator transforms traditional web searching into an intelligent, automated, and user-centric experience
 
## Overview:
To do tasks like searching, clicking, extracting data, and presenting results in an organized manner, the browser agent uses natural language instructions, either spoken or typed, to determine what the user truly wants. In order to navigate websites, fill out forms, click buttons, and carry out intricate web tasks based on natural language descriptions, this process combines browser automation, DOM analysis, and AI models.
For example:
"when we are searching of shoes in amezon"
The agent will: -Use a local LLM to plan the task,
-Open the browser and look up well-known websites,
-extract data like(titles, costs, and ratings),
Analyze the outcomes and present them in a clear, well-organized manner.
The browser functions similarly to a virtual assistant, but instead of searching, it does web work for us.
## Approach:
The approach for building the Web Navigator AI involves:
it takes user queries in natural language and then normalize the input for further processing ,and then the llm interprets user intent,extract key tasks just constraints and output format and then the query converted into executable workflow.
##  Features:
-   **Natural Language Understanding**  
    Users can simply talk or type instruction like:
    
    -   _"Search for laptops under 50k and list top 5"_
        
    -   _"Find today’s top news headlines"_
        
    -   _"Login to my email and check unread messages"_
 
      The system uses a locally running LLM (via Ollama & LangChain) to understand these commands, break them into steps, and plan the required browser actions.
        
-   **Autonomous Web Navigation**:
    Once the instruction process is done it will understand it and uses Playwright to actually:
    - Open websites
    - Fill forms
    - Click buttons
    - Navigate links
    - scrap data
      The system will handle the problems just like a human would but automatically.
-   **Structured Outputs**  
    Extracts relevant data from web pages and returns results in **JSON/CSV/table**  format for further usage.
-   **Local-First Design**  
    Runs entirely on your machine with local LLMs (via **Ollama**, **LangChain**, or other providers).
-   **Job searching agent**
    Searches job portals (LinkedIn, Naukri, Indeed), extracts job details (title, company, salary, location, experience), ranks, and organizes.
-   **Shopping agent**
    Searches multiple e-commerce sites (Amazon, Flipkart, etc.), collects product info (price ,rating,features) , compares,and summarizes.

## Workflow:
![Alt text](<img width="819" height="1382" alt="Web AI Navigator workflow png (2)" src="https://github.com/user-attachments/assets/fa49e61e-9d2b-43ce-9641-7894d159d5dc" />
)


## Tech Stack :
- **Languages :** Python, Node.js  
- **Frontend**: Node.js (Frontend Service),javasript,html,css
- **Backend**: Python (Agent Core, Backend Logic), LangChain/LangGraph (Multi-Agent Orchestration), Ollama (Local LLM Runtime)
- **Instruction Parsing (LLM):**  
  - Ollama (local LLM runtime)  
  - LangChain (for structuring prompts, reasoning, and organizing multi-step workflows)  
  - (Optional) OpenAI / Hugging Face models for fallback or testing  

- **Browser Automation:** Playwright / Selenium / Puppeteer  

- **Database:** PostgreSQL / MongoDB (for storing queries, logs, structured results)  

- **DevOps & Deployment:** GitHub Actions (CI/CD), Docker, cloud hosting  
  

## Prerequisites:

-   Python 3.9+ or Node.js 18+
    
-   Chrome/Chromium installed
    
-   Playwright/Selenium/Puppeteer dependencies installed
    
-   Local LLM runtime (e.g., **Ollama**)

## Future Enhancements:

-   ✅ Multi-step task execution (e.g., "book a train ticket and email me confirmation")
    
-   ✅ Memory of past actions for better context handling
    
-   ✅ Web UI for interactive usage
    
-   ✅ Plug-and-play local LLM model support

## About OneCompiler:
OneCompiler helps coding more **accessible with cloud compiler, simple, and collaborative** for everyone.


# Project Introduction:-
The idea is to build an AI Agent that can take **natural language instructions** from the user, and then autonomously control a browser to fetch and structure information. For example, if a user says _'Search for laptops under 50k and list the top 5'_, our agent will plan the task, browse the web, extract results,compare and return them in a neat structured format.
To achieve this, we are combining a **local LLM for planning** with **browser automation tools** like Playwright or Selenium. We’ve divided our responsibilities into five roles to bring this prototype to life. Let’s walk you through them.

## LLM integration:-
As the "brain" of the project, the LLM will decipher intent, simplify complicated requests, and facilitate a conversational and seamless browsing experience. Furthermore, it will give users context-aware explanations so they are aware of what is happening at every stage. Whether it's completing forms, summarizing content, or comparing data from various websites, the LLM will help close the gap between online activities and human communication.
To put it briefly, the LLM integration transforms the agent into a useful partner who adjusts to the way people naturally interact online, rather than merely a tool.

## Frontend developer:-
“The frontend part is all about the user interface and experience.
We’re going to build a simple website where users can either speak or type their instructions. The AI agent’s responses will be displayed in a structured, easy-to-follow format.
The design will also showcase the agent’s activity and results in real time, with each step unfolding on screen so it feels like an assistant is performing the search right in front of you. If the progress isn’t going in the desired direction, users can stop the process instantly.”

## Backend developer:-
Backend focuses on connecting the AI agent with the frontend without relying on external APIs. The backend will manage direct interactions with the local LLM (via LangChain or Ollama), transforming user instructions into actionable, multi-step plans.

**LLM Orchestration**: The backend ensures prompts are structured, reasoning flows smoothly, and intent is routed to the right specialized agent. This is the essence of Agent Control.

**Automation Trigger**: Oversees browser automation sessions (using Playwright or Selenium), converting the agent’s step-by-step plan into real web actions.

**Security & Logic**: The user has no need of worrying about data leakage, As the LLM runs in the local machine so the data won't go out of the device. It handles authentication, ensures safe processing, and maintains accurate execution of tasks while streaming progress back to the user in real time.


## DevOps Lead:-
we need to make sure our project is executed flawlessly from development to deployment. To keep the database, frontend, and backend organized and manageable by the team, I'll start by establishing a clear repository structure. In order to minimize errors and expedite our workflow, I will also set up CI/CD pipelines so that each code update is automatically tested and deployed.
For hosting, we will use a managed cloud service like MongoDB Atlas or PostgreSQL for the database, Railway or Render for the backend, and Vercel for the frontend. Stability, scalability, and dependability are offered by this configuration.
we will incorporate logging and monitoring tools to track performance, identify issues promptly, and guarantee the agent remains secure in order to keep everything under control. To put it briefly, my job is to ensure that the Web Navigator AI Agent is not only operational but also trustworthy, effective, and prepared for practical application.

## Prototype and Closing Summary (PM/Testing & Documents Lead):-
Lastly, we will oversee our **task assignments, documentation, testing, and pitch preparation** 
### Our model will demonstrate:
Users enter instructions in a **frontend app**.
An LLM-powered **backend service** that translates commands into actions in the browser.
Real-time web data is retrieved by **browser automation**.
A **database** for recording and archiving outcome.  
A **CI/CD pipeline** to maintain dependability and deployability.

## Summary:-
According to the problem statement , if someone wants find information on the web like ex-:best mobiles under 15k they just manually:
- **open browser**
- **type the problem**
- **visit site**
- **check results one by one**
- **collect the information**
 
 This process takes a lot of time.
The main problem is that users want to give simple language instructions and have a system that can do all browsing work automatically for them.

So, the main problem to solve is how to make a system understand what the user wants
So inorder to solve this problem we need an AI agent that can navigate the web,search,click,extract data and give clean answers.
We should build an AI Agent that can take natural language instructions and autonomously drive the web on a local computer. The system should combine a locally running LLM with a browser automation setup such as Chrome Headless or a browser inside a local VM. Users should be able to give simple commands and the agent should execute them by controlling the browser, extracting results, and returning structured outputs.

Uniqueness and impact -:
In this project we are using two main unique ideas-
Job searching agent
Shopping agent
general browsing

From this two ideas -:
-Let us take an example of a person who is searching for a job in different platforms  can prefer this browser so that he can upload his resume once and then he will get to know about jobs based on his resume from different platforms.So, by this the AI agent will be given access for every platform so that it will search jobs for the user according to their resume.
-Similarly a girl want to buy a dress for an occasion can give her prompt exactly so that agenr will search,compares price,rating and features and give the best output.

Together, this forms our **Web Navigator AI Agent** — a powerful tool to make browsing more intelligent and autonomous.

Thank you!"
