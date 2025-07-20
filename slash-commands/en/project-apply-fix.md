flowchart TD
    Start([Start: Fix needed]) --> A["A. Summarize what you will fix<br/>Use exact wording<br/>Unambiguous logic"]
    
    A --> B["B. Check if you know everything needed for the fix"]
    
    B --> B1["Check:<br/>- CLAUDE.md files<br/>- README.md files<br/>- CLAUDE-AVISEO.md"]
    
    B1 --> B2{"All info<br/>available?"}
    
    B2 -->|No| B3["Ask for help<br/>Indicate what is missing"]
    B3 --> B1
    
    B2 -->|Yes| C["C. Confirm:<br/>I have all required information<br/>to execute the fix!"]
    
    C --> D["D. Start execution of the fix"]
    
    D --> D1["Step 1: Specify which changes<br/>in codebase are needed"]
    
    D1 --> D2["Step 2: Create structured plan<br/>with Todos"]
    
    D2 --> D3["Step 3: Show plan with Todos<br/>Ask permission to start"]
    
    D3 --> D3Check{"Permission<br/>received?"}
    
    D3Check -->|No| D3Wait["Wait for permission"]
    D3Wait --> D3Check
    
    D3Check -->|Yes| D4["Step 4: Show list of Todos<br/>Start execution"]
    
    D4 --> TodoLoop["For each Todo:"]
    
    TodoLoop --> D5["Step 5: Create backup of files<br/>to be modified"]
    
    D5 --> D6Execute["Execute Todo"]
    
    D6Execute --> D6["Step 6: Create summary of work done<br/>Update Todo list<br/>Ask permission for next"]
    
    D6 --> D6Check{"Permission for<br/>next Todo?"}
    
    D6Check -->|No| D6Wait["Wait for permission"]
    D6Wait --> D6Check
    
    D6Check -->|Yes| AllDone{"All Todos<br/>completed?"}
    
    AllDone -->|No| TodoLoop
    
    AllDone -->|Yes| D7["Step 7: Ask permission to<br/>delete backups"]
    
    D7 --> D7Check{"Permission to<br/>delete<br/>backups?"}
    
    D7Check -->|No| KeepBackups["Keep backups"]
    D7Check -->|Yes| DeleteBackups["Delete backups"]
    
    KeepBackups --> End([Fix completed])
    DeleteBackups --> End
