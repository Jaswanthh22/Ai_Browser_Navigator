----------------------------------------------------------------

# Web Navigator AI Agent
## An autonomous AI agent that understands natural language and drives the web automatically.

This system combines a **locally running LLM** (for instruction understanding and planning) with a **browser automation setup** (Playwright/Selenium/Puppeteer) to execute user commands.

## Summary
In order to do tasks like searching, clicking, extracting data, and presenting results in an organized manner, the browser agent uses natural language instructions, either spoken or typed, to determine what the user truly wants. In order to navigate websites, fill out forms, click buttons, and carry out intricate web tasks based on natural language descriptions, this process combines browser automation, DOM analysis, and AI models.
For example:
 "Look for laptops under ₹50,000 and make a list of the top five."
The agent will: -Use a local LLM to plan the task,
-Open the browser and look up well-known websites,
-extract pertinent data (titles, costs, and ratings),
Analyze the outcomes and present them in a clear, well-organized table.
The browser functions similarly to a virtual assistant, but instead of searching, it does web work for us.

##  Features

-   **Natural Language Understanding**  
    Users can simply talk or type instruction like:
    
    -   _"Search for laptops under 50k and list top 5"_
        
    -   _"Find today’s top news headlines"_
        
    -   _"Login to my email and check unread messages"_
 
      The system uses a locally running LLM (via Ollama & LangChain) to understand these commands, break them into steps, and plan the required browser actions.
        
-   **Autonomous Web Navigation**  
    Once the instruction process is done it will understand it and uses ..................................{Playwright} to actually:
    - Open websites
    - Fill forms
    - Click buttons
    - Navigate links
    - Scrape data
      The system will handle the problems just like a human would but automatically.
-   **Structured Outputs**  
    Extracts relevant data from web pages and returns results in .......................................**JSON/CSV/table**  format for further usage.
-   **Local-First Design**  
    Runs entirely on your machine with local LLMs (via **Ollama**, **LangChain**, or other providers).
-   **Job searching agent**
    Searches job portals (LinkedIn, Naukri, Indeed), extracts job details (title, company, salary, location, experience), ranks, and organizes.
-   **Shopping agent**
    Searches multiple e-commerce sites (Amazon, Flipkart, etc.), collects product info (price ,rating,features) , compares,and summarizes.
-  

## Tech Stack ......................................................{ jaswanth motha tech stack nuve chudu until Prerequisites }

- **Languages / Orchestration:** Python, Node.js  
- **Frontend**: Node.js (Frontend Service),javasript,html,css
- **Backend & Orchestration**: Python (Agent Core, Backend Logic), LangChain/LangGraph (Multi-Agent Orchestration), Ollama (Local LLM Runtime)
- **Instruction Parsing (LLM):**  
  - Ollama (local LLM runtime)  
  - LangChain (prompt orchestration, reasoning, and step planning)  
  - (Optional) OpenAI / Hugging Face models for fallback or testing  

- **Browser Automation:** Playwright / Selenium / Puppeteer  

- **Database:** PostgreSQL / MongoDB (for storing queries, logs, structured results)  

- **DevOps & Deployment:** GitHub Actions (CI/CD), Docker, cloud hosting  
  

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

OneCompiler helps coding more **accessible, simple, and collaborative** for everyone.


..........................................lisence?

### **1. Project Introduction**:-
The idea is to build an AI Agent that can take **natural language instructions** from the user, and then autonomously control a browser to fetch and structure information. For example, if a user says _'Search for laptops under 50k and list the top 5'_, our agent will plan the task, browse the web, extract results,compare and return them in a neat structured format.
To achieve this, we are combining a **local LLM for planning** with **browser automation tools** like .....................................{Playwright or Selenium}. We’ve divided our responsibilities into five roles to bring this prototype to life. Let’s walk you through them.

### **2. Frontend developer**:
This person is in charge of the **user interface and experience**.
We're going to create a simple website that allows users to voice or type their instructions. The AI agent's output will be presented in a **structured fashion**.
Additionally, we will oversee the **API integration** and show agent activity and outcomes in real time. With each step displayed on the screen, it will seem as though an informed assistant is performing your web search queries directly in front of you. You can immediately halt the process if you notice that the work isn't progressing as you had hoped thanks to this design.

### **3. Lead for Backend**

👤 **Backend Lead is the speaker**  
Designing and implementing the **backend system** is my responsibility.

This entails creating **REST APIs** to link the AI agent and frontend. The **local LLM** will receive user instructions from the backend (via LangChain or Ollama), convert them into actionable steps, and then use Playwright or Selenium to initiate **browser automation**.

I'll also take care of **authentication and business logic**, ensuring that every request is handled securely and effectively.
**API Implementation**: Creates REST APIs to link the AI system and the frontend, guaranteeing effective transmission of commands and status updates.
Using LangChain or Ollama, the local LLM receives instructions, converts them into multi-step plans, and handles **Intent Routing** to specialized agents. This is known as **Agent Control**.
* **Automation Trigger**: Manages browser automation sessions (via Playwright or Selenium), translating planned steps into web actions.
* **Security & Logic**: Ensures secure processing, efficient execution, and accurate streaming of requests to the user.

### **4. Database Lead**

👤 **Speaker: Database Lead**  
"I will plan and oversee the memory and auditing layer of our project as the database lead.

We must **store structured results, user queries, and logs** for analytics and debugging, even though a large portion of the browsing data is real-time. During testing, I'll make sure our database can manage several queries, optimize **queries for speed**, and create the **schema** for storing this data.
In this manner, our AI agent **learns and improves** from past user interactions in addition to responding.
* **Data Storage**: Stores historical queries, structured results, and execution logs for debugging and analytics using PostgreSQL/MongoDB.
* **Schema Design**: Optimizes the schema to manage large amounts of logs and results produced by the multi-agent system.
* **Performance**: Assures that queries are speed-optimized, allowing for scalability for numerous requests at once and opening the door for future analytics to improve agent performance.
  
👤 **Speaker: DevOps Lead** "I am responsible for making sure our project is executed flawlessly from development to deployment. To keep the database, frontend, and backend organized and manageable by the team, I'll start by establishing a clear repository structure. In order to minimize errors and expedite our workflow, I will also set up CI/CD pipelines so that each code update is automatically tested and deployed.
For hosting, we'll use a managed cloud service like MongoDB Atlas or PostgreSQL for the database, Railway or Render for the backend, and Vercel for the frontend. Stability, scalability, and dependability are offered by this configuration.

I'll incorporate logging and monitoring tools to track performance, identify issues promptly, and guarantee the agent remains secure in order to keep everything under control. To put it briefly, my job is to ensure that the Web Navigator AI Agent is not only operational but also trustworthy, effective, and prepared for practical application.

### **6. Prototype and Closing Summary (PM/Testing & Documents Lead)**

**Speaker: PM/Testing & Documents Lead** 👤  
Lastly, I will oversee our **task assignments, documentation, testing, and pitch preparation** in my capacity as PM and Docs Lead.

## Our model will demonstrate:

Users enter instructions in a **frontend app**.
    
An LLM-powered **backend service** that translates commands into actions in the browser.
    
Real-time web data is retrieved by **browser automation**.
    
A **database** for recording and archiving outcomes.
    
A **CI/CD pipeline** to maintain dependability and deployability.
    

Together, this forms our **Web Navigator AI Agent** — a powerful tool to make browsing more intelligent and autonomous.

Thank you!"
