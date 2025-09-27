----------------------------------------------------------------

# Web Navigator AI Agent
## An autonomous AI agent that understands natural language and drives the web automatically.

This system combines a **locally running LLM** (for instruction understanding and planning) with a **browser automation setup** (Playwright/Selenium/Puppeteer) to execute user commands.

## Overview
Browser Agent is a sophisticated Python application that enables users to control web browsers through natural language instructions. It uses a combination of AI models, browser automation, and DOM analysis to navigate websites, fill forms, click buttons, and perform complex web tasks based on natural language descriptions.

The agent features intelligent page analysis, robust error handling, and flexible interaction capabilities, making it ideal for automating repetitive browser tasks, web scraping, site testing, and interactive browsing sessions.

##  Features

-   **Natural Language Understanding**  
    Users can provide simple instructions like in the form of text or speech:
    
    -   _"Search for laptops under 50k and list top 5"_
        
    -   _"Find today’s top news headlines"_
        
    -   _"Login to my email and check unread messages"_
        
-   **Autonomous Web Navigation**  
    The agent plans and executes browser actions such as searching, clicking, filling forms, and scraping data.
    
-   **Structured Outputs**  
    Extracts relevant data from web pages and returns results in JSON/CSV/table format for further usage.
    
-   **Local-First Design**  
    Runs entirely on your machine with local LLMs (via **Ollama**, **LangChain**, or other providers).
-   **Job searching agent**
    Searches job portals (LinkedIn, Naukri, Indeed), extracts job details (title, company, salary, location, experience), ranks, and organizes.
-   **Shopping agent**
    Searches multiple e-commerce sites (Amazon, Flipkart, etc.), collects product info (price ,rating,features) , compares,and summarizes.
-  

## Tech Stack

- **Languages / Orchestration:** Python, Node.js  
- **Frontend**: Node.js (Frontend Service), Vercel/Netlify (Deployment)
- **Backend & Orchestration**: Python (Agent Core, Backend Logic), LangChain/LangGraph (Multi-Agent Orchestration), Ollama (Local LLM Runtime)
- **Instruction Parsing (LLM):**  
  - Ollama (local LLM runtime)  
  - LangChain (prompt orchestration, reasoning, and step planning)  
  - (Optional) OpenAI / Hugging Face models for fallback or testing  

- **Browser Automation:** Playwright / Selenium / Puppeteer  

- **Database:** PostgreSQL / MongoDB (for storing queries, logs, structured results)  

- **DevOps & Deployment:** GitHub Actions (CI/CD), Docker, cloud hosting  
  - Frontend → Vercel/Netlify  
  - Backend → Railway/Render/Heroku  
  - Database → Managed cloud DB service  
    
   ## Installation






### Prerequisites

-   Python 3.9+ or Node.js 18+
    
-   Chrome/Chromium installed
    
-   Playwright/Selenium/Puppeteer dependencies installed
    
-   Local LLM runtime (e.g., **Ollama**)

## Future Enhancements

-   ✅ Multi-step task execution (e.g., "book a train ticket and email me confirmation")
    
-   ✅ Memory of past actions for better context handling
    
-   ✅ Integration with APIs for hybrid workflows
    
-   ✅ Web UI for interactive usage
    
-   ✅ Plug-and-play local LLM model support

## About OneCompiler

OneCompiler helps **12.8M+ developers worldwide** write, run, and share code online.  
We make coding more **accessible, simple, and collaborative** for everyone.

## License

MIT License – feel free to use, modify, and contribute




### **1. Project Introduction (PM/Testing & Docs Lead)**

👤 **Speaker: PM/Testing & Docs Lead**  
"Hello everyone! We are Team Kanyarasi and our hackathon project is **Web Navigator AI Agent**, based on the problem statement HACXPB002 by OneCompiler.

The idea is to build an AI Agent that can take **natural language instructions** from the user, and then autonomously control a browser to fetch and structure information. For example, if a user says _'Search for laptops under 50k and list the top 5'_, our agent will plan the task, browse the web, extract results,compare and return them in a neat structured format.

To achieve this, we are combining a **local LLM for planning** with **browser automation tools** like Playwright or Selenium. We’ve divided our responsibilities into five roles to bring this prototype to life. Let’s walk you through them."

----------

### **2. Frontend developer**

👤 **Speaker: Frontend Lead**  
As the Frontend developer, I’m responsible for the **user interface and experience**.

We are going to build a clean, **responsive web app** where users can simply type or speak their instructions. The results from the AI agent will be displayed in an **organized, readable format**.

I will also manage the API integration to ensure the frontend acts as a transparent window to the AI engine's work. It'll be as if a knowledgeable assistant is carrying out your web search requests right in front of you, with every step visible on the screen. This design allows for instant interruption—you can stop the process the moment you see the work isn't going where you want it to.

----------

### **3. Backend Lead**

👤 **Speaker: Backend Lead**  
"My role is to design and implement the **backend system**.

This involves building **REST APIs** that connect the frontend to the AI agent. The backend will pass user instructions to the **local LLM** (through LangChain or Ollama), translate those into actionable steps, and then trigger **browser automation** via Playwright or Selenium.

Additionally, I’ll handle **authentication and business logic**, making sure each request is securely processed and efficiently executed."
**API Implementation**: Builds REST APIs to connect the frontend to the AI system, ensuring efficient communication of instructions and status updates.
* **Agent Control**: Passes instructions to the local LLM (via LangChain or Ollama), translating them into multi-step plans and handling **Intent Routing** to specialized agents.
* **Automation Trigger**: Manages browser automation sessions (via Playwright or Selenium), translating planned steps into web actions.
* **Security & Logic**: Ensures secure processing, efficient execution, and accurate streaming of requests to the user.
----------

### **4. Database Lead**

👤 **Speaker: Database Lead**  
"As the Database Lead, I’ll design and manage the system's memory and auditing layer of our project.

While much of the browsing data is real-time, we also need to **store structured results, user queries, and logs** for analytics and debugging. I’ll design the **schema** for storing this information, optimize **queries for speed**, and ensure our database can handle multiple queries during testing.

This way, our AI agent doesn’t just respond — it also **learns and improves** from stored user interactions."

* **Data Storage**: Uses PostgreSQL/MongoDB to store structured results, historical queries, and execution logs for analytics and debugging.
* **Schema Design**: Optimizes schema to handle high volumes of logs and results generated by the multi-agent system.
* **Performance**: Ensures queries are optimized for speed, supporting scalability for multiple concurrent requests and enabling future analytics to enhance agent performance.

### **5. DevOps/Deployment Lead**

👤 **Speaker: DevOps Lead**  
"My responsibility is to make sure everything runs **smoothly in development and deployment**.

I’ll set up a clean **repository structure** with separate folders for frontend, backend, and database. Using **CI/CD pipelines**, every change we push will be automatically tested and deployed to staging environments.

For hosting, we’ll use -------- for the frontend, ---------- for the backend, and a managed cloud service for the database. I’ll also integrate **monitoring and logging**, so we can track the agent’s performance and errors in real-time."

----------

### **6. Closing & Prototype Summary (PM/Testing & Docs Lead)**

👤 **Speaker: PM/Testing & Docs Lead**  
"Finally, as PM and Docs Lead, I’ll manage our **task assignments, documentation, testing, and pitch preparation**.

## Our prototype will showcase:

-   A **frontend app** where users type instructions.
    
-   A **backend service** powered by an LLM that converts instructions into browser actions.
    
-   **Browser automation** that fetches real-time web data.
    
-   A **database** to log and store results.
    
-   A **CI/CD pipeline** to keep everything reliable and deployable.
    

Together, this forms our **Web Navigator AI Agent** — a powerful tool to make browsing more intelligent and autonomous.

Thank you!"
