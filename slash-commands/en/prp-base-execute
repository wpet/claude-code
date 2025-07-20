# Execute BASE PRP

Implement a feature using the PRP file.

## PRP File: $ARGUMENTS

## Workflow

flowchart TD
    Start([Start: Execute BASE PRP]) --> Input["Receive PRP File:<br/>ARGUMENTS"]
    
    Input --> LoadPRP["Load PRP"]
    
    LoadPRP --> LP1["Read specified PRP file"]
    LP1 --> LP2["Understand all context and requirements"]
    LP2 --> LP3["Follow all instructions in PRP"]
    LP3 --> LP4["Check if all context available"]
    
    LP4 --> ContextCheck{"All needed context<br/>available?"}
    
    ContextCheck -->|No| ExtendResearch["Extend research if needed"]
    ExtendResearch --> WebSearch["Do more web searches"]
    WebSearch --> CodebaseExplore["Explore codebase further"]
    CodebaseExplore --> LP4
    
    ContextCheck -->|Yes| UltraThink["ULTRATHINK Phase"]
    
    UltraThink --> UT1["Create comprehensive plan<br/>addressing all requirements"]
    UT1 --> UT2["Break down PRP into clear todos<br/>using TodoWrite tool"]
    UT2 --> UT3["Use agents, subagents<br/>and batchtool"]
    UT3 --> UT4["Ensure EXTREMELY CLEAR tasks<br/>for subagents"]
    UT4 --> UT5["Make sure each subagent<br/>reads PRP and understands context"]
    UT5 --> UT6["Identify implementation patterns<br/>from existing code"]
    UT6 --> UT7["Gather real context for imports,<br/>file names, function names"]
    
    UT7 --> PlanReady{"Plan comprehensive<br/>and clear?"}
    
    PlanReady -->|No| RefineP["Refine plan"]
    RefineP --> UT1
    
    PlanReady -->|Yes| Execute["Execute the plan"]
    
    Execute --> E1["Execute PRP step by step"]
    E1 --> E2["Implement all the code"]
    
    E2 --> ImplementCheck{"Implementation<br/>complete?"}
    
    ImplementCheck -->|No| ContinueImpl["Continue implementation"]
    ContinueImpl --> E1
    
    ImplementCheck -->|Yes| Validate["Validate"]
    
    Validate --> V1["Run each validation command"]
    V1 --> V2["Check validation results"]
    
    V2 --> ValidationPass{"All validations<br/>pass?"}
    
    ValidationPass -->|No| V3["Fix failures using<br/>error patterns in PRP"]
    V3 --> V4["Re-run validations"]
    V4 --> V2
    
    ValidationPass -->|Yes| V5["Re-read PRP to validate<br/>implementation meets requirements"]
    
    V5 --> RequirementsCheck{"Implementation meets<br/>all requirements?"}
    
    RequirementsCheck -->|No| FixReq["Fix requirement gaps"]
    FixReq --> Execute
    
    RequirementsCheck -->|Yes| Complete["Complete Phase"]
    
    Complete --> C1["Ensure all checklist items done"]
    C1 --> ChecklistDone{"All checklist<br/>items complete?"}
    
    ChecklistDone -->|No| CompleteItems["Complete missing items"]
    CompleteItems --> C1
    
    ChecklistDone -->|Yes| C2["Run final validation suite"]
    
    C2 --> FinalValidation{"Final validation<br/>passes?"}
    
    FinalValidation -->|No| FixFinal["Fix final issues"]
    FixFinal --> Validate
    
    FinalValidation -->|Yes| C3["Report completion status"]
    C3 --> C4["Read PRP again to ensure<br/>everything implemented"]
    
    C4 --> FinalCheck{"Everything<br/>implemented correctly?"}
    
    FinalCheck -->|No| IdentifyGaps["Identify implementation gaps"]
    IdentifyGaps --> Execute
    
    FinalCheck -->|Yes| Success["Implementation successful"]
    
    Success --> RefOption{"Need to reference<br/>PRP again?"}
    
    RefOption -->|Yes| Reference["Reference the PRP"]
    Reference --> ReviewAgain["Review specific sections"]
    ReviewAgain --> RefOption
    
    RefOption -->|No| End([End: PRP Executed Successfully])
    
    style Start fill:#90EE90
    style End fill:#90EE90
    style UltraThink fill:#FFB6C1
    style Success fill:#87CEEB
    style ContextCheck fill:#FFE4B5
    style PlanReady fill:#FFE4B5
    style ImplementCheck fill:#FFE4B5
    style ValidationPass fill:#FFE4B5
    style RequirementsCheck fill:#FFE4B5
    style ChecklistDone fill:#FFE4B5
    style FinalValidation fill:#FFE4B5
    style FinalCheck fill:#FFE4B5
    style RefOption fill:#FFE4B5
