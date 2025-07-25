# Vertaal django.po naar Nederlands

## ## django.po bestand: $ARGUMENTS

flowchart TD
    Start([Start: Django.po translation to Dutch]) --> Receive["Receive django.po file"]
    
    Receive --> CreateBackup["Create backup of django.po<br/>to django.po-backup"]
    
    CreateBackup --> BackupCheck{"Backup successfully<br/>created?"}
    
    BackupCheck -->|No| BackupError["Error: Cannot create backup"]
    BackupError --> End([End: Process aborted])
    
    BackupCheck -->|Yes| PrepareProcessing["Prepare processing:<br/>Divide file into 10 equal blocks<br/>one for each sub-agent<br/>with overlap between blocks"]
    
    PrepareProcessing --> AssignBlocks["Assign each block<br/>to a specific sub-agent"]
    
    AssignBlocks --> StartAgents["Start 10 sub-agents<br/>for parallel processing"]
    
    StartAgents --> Agent1["Sub-agent 1<br/>Process block 1/10"]
    StartAgents --> Agent2["Sub-agent 2<br/>Process block 2/10"]
    StartAgents --> Agent3["Sub-agent 3<br/>Process block 3/10"]
    StartAgents --> Agent4["Sub-agent 4<br/>Process block 4/10"]
    StartAgents --> Agent5["Sub-agent 5<br/>Process block 5/10"]
    StartAgents --> Agent6["Sub-agent 6<br/>Process block 6/10"]
    StartAgents --> Agent7["Sub-agent 7<br/>Process block 7/10"]
    StartAgents --> Agent8["Sub-agent 8<br/>Process block 8/10"]
    StartAgents --> Agent9["Sub-agent 9<br/>Process block 9/10"]
    StartAgents --> Agent10["Sub-agent 10<br/>Process block 10/10"]
    
    Agent1 --> ProcessAgent1{{"Process assigned block:<br/>- Check fuzzy entries<br/>- Check empty translations<br/>- Remove #~ lines<br/>- Translate to Dutch<br/>- Save as block-1"}}
    Agent2 --> ProcessAgent2{{"Process assigned block:<br/>- Check fuzzy entries<br/>- Check empty translations<br/>- Remove #~ lines<br/>- Translate to Dutch<br/>- Save as block-2"}}
    Agent3 --> ProcessAgent3{{"Process assigned block:<br/>- Check fuzzy entries<br/>- Check empty translations<br/>- Remove #~ lines<br/>- Translate to Dutch<br/>- Save as block-3"}}
    Agent4 --> ProcessAgent4{{"Process assigned block:<br/>- Check fuzzy entries<br/>- Check empty translations<br/>- Remove #~ lines<br/>- Translate to Dutch<br/>- Save as block-4"}}
    Agent5 --> ProcessAgent5{{"Process assigned block:<br/>- Check fuzzy entries<br/>- Check empty translations<br/>- Remove #~ lines<br/>- Translate to Dutch<br/>- Save as block-5"}}
    Agent6 --> ProcessAgent6{{"Process assigned block:<br/>- Check fuzzy entries<br/>- Check empty translations<br/>- Remove #~ lines<br/>- Translate to Dutch<br/>- Save as block-6"}}
    Agent7 --> ProcessAgent7{{"Process assigned block:<br/>- Check fuzzy entries<br/>- Check empty translations<br/>- Remove #~ lines<br/>- Translate to Dutch<br/>- Save as block-7"}}
    Agent8 --> ProcessAgent8{{"Process assigned block:<br/>- Check fuzzy entries<br/>- Check empty translations<br/>- Remove #~ lines<br/>- Translate to Dutch<br/>- Save as block-8"}}
    Agent9 --> ProcessAgent9{{"Process assigned block:<br/>- Check fuzzy entries<br/>- Check empty translations<br/>- Remove #~ lines<br/>- Translate to Dutch<br/>- Save as block-9"}}
    Agent10 --> ProcessAgent10{{"Process assigned block:<br/>- Check fuzzy entries<br/>- Check empty translations<br/>- Remove #~ lines<br/>- Translate to Dutch<br/>- Save as block-10"}}
    
    ProcessAgent1 --> WaitForAll["Wait for all sub-agents to complete"]
    ProcessAgent2 --> WaitForAll
    ProcessAgent3 --> WaitForAll
    ProcessAgent4 --> WaitForAll
    ProcessAgent5 --> WaitForAll
    ProcessAgent6 --> WaitForAll
    ProcessAgent7 --> WaitForAll
    ProcessAgent8 --> WaitForAll
    ProcessAgent9 --> WaitForAll
    ProcessAgent10 --> WaitForAll
    
    WaitForAll --> AllComplete{"All sub-agents<br/>completed?"}
    
    AllComplete -->|No| CheckTimeout{"Timeout<br/>reached?"}
    CheckTimeout -->|Yes| HandleTimeout["Identify hanging agents<br/>Redistribute work"]
    HandleTimeout --> WaitForAll
    CheckTimeout -->|No| WaitForAll
    
    AllComplete -->|Yes| PlayAudio["Play audio file:<br/>.claude/audio/ready.mp3"]
    
    PlayAudio --> AudioCheck{"Audio played?"}
    
    AudioCheck -->|No| AudioRetry["Try audio again"]
    AudioRetry --> PlayAudio
    
    AudioCheck -->|Yes| MergeBlocks["Merge all 10 blocks<br/>in correct order (1-10)<br/>Remove duplicate lines from overlap"]
    
    MergeBlocks --> WriteFile["Write merged result<br/>over original django.po"]
    
    WriteFile --> WriteCheck{"File successfully<br/>overwritten?"}
    
    WriteCheck -->|No| WriteError["Error writing file"]
    WriteError --> RestoreBackup["Restore from backup"]
    RestoreBackup --> End
    
    WriteCheck -->|Yes| AskUser["Ask user:<br/>Is the translation acceptable?"]
    
    AskUser --> UserResponse{"User<br/>confirms?"}
    
    UserResponse -->|No| KeepBackup["Keep backup for<br/>possible corrections"]
    KeepBackup --> EndWithBackup([End: Translation completed<br/>Backup retained])
    
    UserResponse -->|Yes| DeleteBackup["Delete django.po-backup"]
    
    DeleteBackup --> DeleteCheck{"Backup successfully<br/>deleted?"}
    
    DeleteCheck -->|No| DeleteWarning["Warning:<br/>Backup could not be deleted"]
    DeleteWarning --> EndWithWarning([End: Translation completed<br/>Delete backup manually])
    
    DeleteCheck -->|Yes| Success([End: Translation successful<br/>Backup deleted])
    
    style Start fill:#90EE90
    style Success fill:#90EE90
    style EndWithBackup fill:#87CEEB
    style EndWithWarning fill:#FFE4B5
    style End fill:#FF6B6B
    style StartAgents fill:#FFB6C1
    style WaitForAll fill:#FFB6C1
    style BackupCheck fill:#FFE4B5
    style AllComplete fill:#FFE4B5
    style CheckTimeout fill:#FFE4B5
    style AudioCheck fill:#FFE4B5
    style WriteCheck fill:#FFE4B5
    style UserResponse fill:#FFE4B5
    style DeleteCheck fill:#FFE4B5
    style ProcessAgent1 fill:#E6E6FA
    style ProcessAgent2 fill:#E6E6FA
    style ProcessAgent3 fill:#E6E6FA
    style ProcessAgent4 fill:#E6E6FA
    style ProcessAgent5 fill:#E6E6FA
    style ProcessAgent6 fill:#E6E6FA
    style ProcessAgent7 fill:#E6E6FA
    style ProcessAgent8 fill:#E6E6FA
    style ProcessAgent9 fill:#E6E6FA
    style ProcessAgent10 fill:#E6E6FA
