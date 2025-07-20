# Uitvoeren BASE PRP

Implementeer een feature met behulp van het PRP bestand.

## PRP Bestand: $ARGUMENTS

## Workflow

flowchart TD
    Start([Start: Uitvoeren BASE PRP]) --> Input["Ontvang PRP Bestand:<br/>ARGUMENTEN"]
    
    Input --> LoadPRP["Laad PRP"]
    
    LoadPRP --> LP1["Lees gespecificeerd PRP bestand"]
    LP1 --> LP2["Begrijp alle context en vereisten"]
    LP2 --> LP3["Volg alle instructies in PRP"]
    LP3 --> LP4["Controleer of alle context beschikbaar is"]
    
    LP4 --> ContextCheck{"Alle benodigde context<br/>beschikbaar?"}
    
    ContextCheck -->|Nee| ExtendResearch["Breid onderzoek uit indien nodig"]
    ExtendResearch --> WebSearch["Doe meer webzoekopdrachten"]
    WebSearch --> CodebaseExplore["Verken codebase verder"]
    CodebaseExplore --> LP4
    
    ContextCheck -->|Ja| UltraThink["ULTRADENK Fase"]
    
    UltraThink --> UT1["Maak uitgebreid plan<br/>dat alle vereisten adresseert"]
    UT1 --> UT2["Verdeel PRP in duidelijke todos<br/>met TodoWrite tool"]
    UT2 --> UT3["Gebruik agents, subagents<br/>en batchtool"]
    UT3 --> UT4["Zorg voor EXTREEM DUIDELIJKE taken<br/>voor subagents"]
    UT4 --> UT5["Zorg dat elke subagent<br/>PRP leest en context begrijpt"]
    UT5 --> UT6["Identificeer implementatiepatronen<br/>uit bestaande code"]
    UT6 --> UT7["Verzamel echte context voor imports,<br/>bestandsnamen, functienamen"]
    
    UT7 --> PlanReady{"Plan uitgebreid<br/>en duidelijk?"}
    
    PlanReady -->|Nee| RefineP["Verfijn plan"]
    RefineP --> UT1
    
    PlanReady -->|Ja| Execute["Voer het plan uit"]
    
    Execute --> E1["Voer PRP stap voor stap uit"]
    E1 --> E2["Implementeer alle code"]
    
    E2 --> ImplementCheck{"Implementatie<br/>compleet?"}
    
    ImplementCheck -->|Nee| ContinueImpl["Ga door met implementeren"]
    ContinueImpl --> E1
    
    ImplementCheck -->|Ja| Validate["Valideer"]
    
    Validate --> V1["Voer elk validatiecommando uit"]
    V1 --> V2["Controleer validatieresultaten"]
    
    V2 --> ValidationPass{"Alle validaties<br/>geslaagd?"}
    
    ValidationPass -->|Nee| V3["Herstel fouten met<br/>foutpatronen uit PRP"]
    V3 --> V4["Voer validaties opnieuw uit"]
    V4 --> V2
    
    ValidationPass -->|Ja| V5["Herlees PRP om te valideren dat<br/>implementatie aan vereisten voldoet"]
    
    V5 --> RequirementsCheck{"Implementatie voldoet<br/>aan alle vereisten?"}
    
    RequirementsCheck -->|Nee| FixReq["Herstel ontbrekende vereisten"]
    FixReq --> Execute
    
    RequirementsCheck -->|Ja| Complete["Voltooiingsfase"]
    
    Complete --> C1["Zorg dat alle checklist items gedaan zijn"]
    C1 --> ChecklistDone{"Alle checklist<br/>items compleet?"}
    
    ChecklistDone -->|Nee| CompleteItems["Voltooi ontbrekende items"]
    CompleteItems --> C1
    
    ChecklistDone -->|Ja| C2["Voer finale validatiesuite uit"]
    
    C2 --> FinalValidation{"Finale validatie<br/>geslaagd?"}
    
    FinalValidation -->|Nee| FixFinal["Herstel finale problemen"]
    FixFinal --> Validate
    
    FinalValidation -->|Ja| C3["Rapporteer voltooiingsstatus"]
    C3 --> C4["Lees PRP opnieuw om te verzekeren<br/>dat alles geïmplementeerd is"]
    
    C4 --> FinalCheck{"Alles correct<br/>geïmplementeerd?"}
    
    FinalCheck -->|Nee| IdentifyGaps["Identificeer implementatiehiaten"]
    IdentifyGaps --> Execute
    
    FinalCheck -->|Ja| Success["Implementatie succesvol"]
    
    Success --> RefOption{"Nodig om PRP<br/>opnieuw te raadplegen?"}
    
    RefOption -->|Ja| Reference["Raadpleeg de PRP"]
    Reference --> ReviewAgain["Bekijk specifieke secties"]
    ReviewAgain --> RefOption
    
    RefOption -->|Nee| End([Einde: PRP Succesvol Uitgevoerd])
    
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
