

----------------------------------------------------------------

## Web Navigator AI Agent
An autonomous AI-powered agent that takes **natural language instructions** and drives the web automatically on a local machine.  
This system combines a **locally running LLM** (for instruction understanding and planning) with a **browser automation setup** (Playwright/Selenium/Puppeteer) to execute user commands.

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
