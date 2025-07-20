# Create BASE PRP

## Feature: $ARGUMENTS

## Workflow

flowchart TD
    Start([Start: Create BASE PRP]) --> Input["Receive ARGUMENTS<br/>Feature specification"]
    
    Input --> ResearchStart["Begin Research Process<br/>Optimize for success, not speed"]
    
    ResearchStart --> CodebaseAnalysis["Codebase Analysis in Depth"]
    
    CodebaseAnalysis --> CA1["Create clear todos for codebase search"]
    CA1 --> CA2["Spawn subagents for pattern search"]
    CA2 --> CA3["Identify necessary files to reference"]
    CA3 --> CA4["Note existing conventions"]
    CA4 --> CA5["Check test patterns for validation"]
    CA5 --> CA6["Read CLAUDE.md files:<br/>./CLAUDE.md<br/>./app_name/CLAUDE.md<br/>claude_md_files/CLAUDE-AVISEO.md"]
    CA6 --> CA7["Use batch tools for deep pattern search"]
    
    CA7 --> CACheck{"Codebase analysis<br/>complete?"}
    CACheck -->|No| CAMissing["Identify missing elements"]
    CAMissing --> CA1
    
    CACheck -->|Yes| ExternalResearch["External Research at Scale"]
    
    ExternalResearch --> ER1["Create todos for external research"]
    ER1 --> ER2["Spawn subagents for online research"]
    ER2 --> ER3["Gather library documentation URLs"]
    ER3 --> ER4["Find implementation examples<br/>GitHub/StackOverflow/blogs"]
    ER4 --> ER5["Document best practices"]
    ER5 --> ER6["Note common pitfalls"]
    ER6 --> ERCritical{"Critical documentation<br/>found?"}
    
    ERCritical -->|Yes| ER7["Add .md files to PRPs/ai_docs<br/>Reference in PRP with reasoning"]
    ERCritical -->|No| ER8["Continue with gathered info"]
    
    ER7 --> ERCheck{"External research<br/>complete?"}
    ER8 --> ERCheck
    
    ERCheck -->|No| ERMissing["Identify research gaps"]
    ERMissing --> ER1
    
    ERCheck -->|Yes| ClarificationCheck{"User clarification<br/>needed?"}
    
    ClarificationCheck -->|Yes| UC1["Ask user for clarification"]
    UC1 --> UCWait["Wait for user response"]
    UCWait --> UCReceived{"Clarification<br/>received?"}
    UCReceived -->|No| UCWait
    UCReceived -->|Yes| UCProcess["Process clarification"]
    UCProcess --> AllResearchDone
    
    ClarificationCheck -->|No| AllResearchDone["All research completed"]
    
    AllResearchDone --> UltraThink["ULTRATHINK about PRP approach<br/>Plan detailed todos"]
    
    UltraThink --> PRPGen["Begin PRP Generation<br/>Using PRPs/templates/prp_base.md"]
    
    PRPGen --> Context["Add Critical Context:<br/>Documentation URLs<br/>Code examples<br/>Gotchas<br/>Patterns<br/>Best practices"]
    
    Context --> Blueprint["Create Implementation Blueprint:<br/>Pseudocode approach<br/>Reference real files<br/>Error handling strategy<br/>Ordered task list"]
    
    Blueprint --> Validation["Define Validation Gates:<br/>ruff check --fix<br/>mypy .<br/>pytest tests/ -v<br/>Additional creative gates"]
    
    Validation --> ValCheck{"All validation gates<br/>executable by AI?"}
    
    ValCheck -->|No| ValFix["Fix validation gates<br/>Make executable"]
    ValFix --> Validation
    
    ValCheck -->|Yes| SavePRP["Save PRP to:<br/>PRPs/output/create/feature-name.md"]
    
    SavePRP --> QualityCheck["Run Quality Checklist"]
    
    QualityCheck --> QC1{"Context included?"}
    QC1 -->|No| QCFix1["Add missing context"]
    QCFix1 --> Context
    
    QC1 -->|Yes| QC2{"Validation gates<br/>executable?"}
    QC2 -->|No| QCFix2["Fix validation gates"]
    QCFix2 --> Validation
    
    QC2 -->|Yes| QC3{"References existing<br/>patterns?"}
    QC3 -->|No| QCFix3["Add pattern references"]
    QCFix3 --> Context
    
    QC3 -->|Yes| QC4{"Clear implementation<br/>path?"}
    QC4 -->|No| QCFix4["Clarify implementation"]
    QCFix4 --> Blueprint
    
    QC4 -->|Yes| QC5{"Error handling<br/>documented?"}
    QC5 -->|No| QCFix5["Add error handling"]
    QCFix5 --> Blueprint
    
    QC5 -->|Yes| Score["Score PRP confidence<br/>Scale 1 to 10"]
    
    Score --> ScoreCheck{"Score >= 8?"}
    
    ScoreCheck -->|No| Improve["Identify improvements needed"]
    Improve --> ImprovementType{"What needs<br/>improvement?"}
    
    ImprovementType -->|Research| ResearchStart
    ImprovementType -->|Context| Context
    ImprovementType -->|Implementation| Blueprint
    ImprovementType -->|Validation| Validation
    
    ScoreCheck -->|Yes| Complete["PRP Complete<br/>Ready for one-pass implementation"]
    
    Complete --> End([End: PRP Generated])
    
    style Start fill:#90EE90
    style End fill:#90EE90
    style UltraThink fill:#FFB6C1
    style AllResearchDone fill:#87CEEB
    style CACheck fill:#FFE4B5
    style ERCheck fill:#FFE4B5
    style ClarificationCheck fill:#FFE4B5
    style ValCheck fill:#FFE4B5
    style ScoreCheck fill:#FFE4B5
    style QC1 fill:#FFE4B5
    style QC2 fill:#FFE4B5
    style QC3 fill:#FFE4B5
    style QC4 fill:#FFE4B5
    style QC5 fill:#FFE4B5
