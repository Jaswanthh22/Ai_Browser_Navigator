----------------------------------------------------------------

## Web Navigator AI Agent
An autonomous AI-powered agent that takes **natural language instructions** and drives the web automatically on a local machine.  
This system combines a **locally running LLM** (for instruction understanding and planning) with a **browser automation setup** (Playwright/Selenium/Puppeteer) to execute user commands.

## Overview
Browser Agent is a sophisticated Python application that enables users to control web browsers through natural language instructions. It uses a combination of AI models, browser automation, and DOM analysis to navigate websites, fill forms, click buttons, and perform complex web tasks based on natural language descriptions.

The agent features intelligent page analysis, robust error handling, and flexible interaction capabilities, making it ideal for automating repetitive browser tasks, web scraping, site testing, and interactive browsing sessions.

##  Features

-   **Natural Language Understanding**  
    Users can provide simple instructions like:
    
    -   _"Search for laptops under 50k and list top 5"_
        
    -   _"Find today’s top news headlines"_
        
    -   _"Login to my email and check unread messages"_
        
-   **Autonomous Web Navigation**  
    The agent plans and executes browser actions such as searching, clicking, filling forms, and scraping data.
    
-   **Structured Outputs**  
    Extracts relevant data from web pages and returns results in JSON/CSV/table format for further usage.
    
-   **Local-First Design**  
    Runs entirely on your machine with local LLMs (via **Ollama**, **LangChain**, or other providers).

## Tech Stack

-   **Orchestration:** Python / Node.js
    
-   **Instruction Parsing (LLM):**
    
    
        
-   **Browser Automation:**





    
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

MIT License – feel free to use, modify, and contribute.





vedio speech:

### **1. Project Introduction (PM/Testing & Docs Lead)**

👤 **Speaker: PM/Testing & Docs Lead**  
"Hello everyone! We are Team ----------- and our hackathon project is **Web Navigator AI Agent**, based on the problem statement HACXPB002 by OneCompiler.

The idea is to build an AI Agent that can take **natural language instructions** from the user, and then autonomously control a browser to fetch and structure information. For example, if a user says _'Search for laptops under 50k and list the top 5'_, our agent will plan the task, browse the web, extract results, and return them in a neat structured format.

To achieve this, we are combining a **local LLM for planning** with **browser automation tools** like Playwright or Selenium. We’ve divided our responsibilities into five roles to bring this prototype to life. Let’s walk you through them."

----------

### **2. Frontend Lead**

👤 **Speaker: Frontend Lead**  
"As the Frontend Lead, I’m responsible for the **user interface and experience**.

We are designing a clean, **responsive web app** where users can simply type or speak their instructions. The results from the AI agent will be displayed in an **organized, readable format**, such as tables or cards.

I’ll also handle **API integration** so that the frontend communicates smoothly with our backend AI engine, ensuring the user feels like they’re chatting with a smart assistant that can browse the web on their behalf."

----------

### **3. Backend Lead**

👤 **Speaker: Backend Lead**  
"My role is to design and implement the **backend system**.

This involves building **REST APIs** that connect the frontend to the AI agent. The backend will pass user instructions to the **local LLM** (through LangChain or Ollama), translate those into actionable steps, and then trigger **browser automation** via Playwright or Selenium.

Additionally, I’ll handle **authentication and business logic**, making sure each request is securely processed and efficiently executed."

----------

### **4. Database Lead**

👤 **Speaker: Database Lead**  
"As the Database Lead, I’ll design and manage the ----------- of our project.

While much of the browsing data is real-time, we also need to **store structured results, user queries, and logs** for analytics and debugging. I’ll design the **schema** for storing this information, optimize **queries for speed**, and ensure our database can handle multiple queries during testing.

This way, our AI agent doesn’t just respond — it also **learns and improves** from stored user interactions."

----------

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
