# Maak BASE PRP

## Feature: $ARGUMENTS

## Workflow

flowchart TD
    Start([Start: Maak BASE PRP]) --> Input["Ontvang ARGUMENTEN<br/>Feature specificatie"]
    
    Input --> ResearchStart["Begin Onderzoeksproces<br/>Optimaliseer voor succes, niet snelheid"]
    
    ResearchStart --> CodebaseAnalysis["Codebase Analyse in Detail"]
    
    CodebaseAnalysis --> CA1["Maak duidelijke todos voor codebase zoeken"]
    CA1 --> CA2["Start subagents voor patroon zoeken"]
    CA2 --> CA3["Identificeer benodigde bestanden om te refereren"]
    CA3 --> CA4["Noteer bestaande conventies"]
    CA4 --> CA5["Controleer testpatronen voor validatie"]
    CA5 --> CA6["Lees CLAUDE.md bestanden:<br/>./CLAUDE.md<br/>./app_name/CLAUDE.md<br/>claude_md_files/CLAUDE-AVISEO.md"]
    CA6 --> CA7["Gebruik batch tools voor diep patroon zoeken"]
    
    CA7 --> CACheck{"Codebase analyse<br/>compleet?"}
    CACheck -->|Nee| CAMissing["Identificeer ontbrekende elementen"]
    CAMissing --> CA1
    
    CACheck -->|Ja| ExternalResearch["Extern Onderzoek op Schaal"]
    
    ExternalResearch --> ER1["Maak todos voor extern onderzoek"]
    ER1 --> ER2["Start subagents voor online onderzoek"]
    ER2 --> ER3["Verzamel library documentatie URLs"]
    ER3 --> ER4["Vind implementatie voorbeelden<br/>GitHub/StackOverflow/blogs"]
    ER4 --> ER5["Documenteer best practices"]
    ER5 --> ER6["Noteer veelvoorkomende valkuilen"]
    ER6 --> ERCritical{"Kritieke documentatie<br/>gevonden?"}
    
    ERCritical -->|Ja| ER7["Voeg .md bestanden toe aan PRPs/ai_docs<br/>Refereer in PRP met redenering"]
    ERCritical -->|Nee| ER8["Ga door met verzamelde info"]
    
    ER7 --> ERCheck{"Extern onderzoek<br/>compleet?"}
    ER8 --> ERCheck
    
    ERCheck -->|Nee| ERMissing["Identificeer onderzoekshiaten"]
    ERMissing --> ER1
    
    ERCheck -->|Ja| ClarificationCheck{"Gebruiker verduidelijking<br/>nodig?"}
    
    ClarificationCheck -->|Ja| UC1["Vraag gebruiker om verduidelijking"]
    UC1 --> UCWait["Wacht op gebruiker reactie"]
    UCWait --> UCReceived{"Verduidelijking<br/>ontvangen?"}
    UCReceived -->|Nee| UCWait
    UCReceived -->|Ja| UCProcess["Verwerk verduidelijking"]
    UCProcess --> AllResearchDone
    
    ClarificationCheck -->|Nee| AllResearchDone["Alle onderzoek voltooid"]
    
    AllResearchDone --> UltraThink["ULTRADENK over PRP aanpak<br/>Plan gedetailleerde todos"]
    
    UltraThink --> PRPGen["Begin PRP Generatie<br/>Gebruik PRPs/templates/prp_base.md"]
    
    PRPGen --> Context["Voeg Kritieke Context toe:<br/>Documentatie URLs<br/>Code voorbeelden<br/>Valkuilen<br/>Patronen<br/>Best practices"]
    
    Context --> Blueprint["Maak Implementatie Blauwdruk:<br/>Pseudocode aanpak<br/>Refereer echte bestanden<br/>Foutafhandeling strategie<br/>Geordende takenlijst"]
    
    Blueprint --> Validation["Definieer Validatie Poorten:<br/>ruff check --fix<br/>mypy .<br/>pytest tests/ -v<br/>Extra creatieve poorten"]
    
    Validation --> ValCheck{"Alle validatie poorten<br/>uitvoerbaar door AI?"}
    
    ValCheck -->|Nee| ValFix["Herstel validatie poorten<br/>Maak uitvoerbaar"]
    ValFix --> Validation
    
    ValCheck -->|Ja| SavePRP["Bewaar PRP naar:<br/>PRPs/output/create/feature-naam.md"]
    
    SavePRP --> QualityCheck["Voer Kwaliteits Checklist uit"]
    
    QualityCheck --> QC1{"Context inbegrepen?"}
    QC1 -->|Nee| QCFix1["Voeg ontbrekende context toe"]
    QCFix1 --> Context
    
    QC1 -->|Ja| QC2{"Validatie poorten<br/>uitvoerbaar?"}
    QC2 -->|Nee| QCFix2["Herstel validatie poorten"]
    QCFix2 --> Validation
    
    QC2 -->|Ja| QC3{"Refereert bestaande<br/>patronen?"}
    QC3 -->|Nee| QCFix3["Voeg patroon referenties toe"]
    QCFix3 --> Context
    
    QC3 -->|Ja| QC4{"Duidelijk implementatie<br/>pad?"}
    QC4 -->|Nee| QCFix4["Verduidelijk implementatie"]
    QCFix4 --> Blueprint
    
    QC4 -->|Ja| QC5{"Foutafhandeling<br/>gedocumenteerd?"}
    QC5 -->|Nee| QCFix5["Voeg foutafhandeling toe"]
    QCFix5 --> Blueprint
    
    QC5 -->|Ja| Score["Score PRP vertrouwen<br/>Schaal 1 tot 10"]
    
    Score --> ScoreCheck{"Score >= 8?"}
    
    ScoreCheck -->|Nee| Improve["Identificeer benodigde verbeteringen"]
    Improve --> ImprovementType{"Wat heeft<br/>verbetering nodig?"}
    
    ImprovementType -->|Onderzoek| ResearchStart
    ImprovementType -->|Context| Context
    ImprovementType -->|Implementatie| Blueprint
    ImprovementType -->|Validatie| Validation
    
    ScoreCheck -->|Ja| Complete["PRP Compleet<br/>Klaar voor één-stap implementatie"]
    
    Complete --> End([Einde: PRP Gegenereerd])
    
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
