# Stappenplan voor het uitvoeren van de fix

flowchart TD
    Start([Start: Fix nodig]) --> A["A. Vat samen wat je gaat fixen<br/>Gebruik exacte bewoordingen<br/>Niet-dubbelzinnige logica"]
    
    A --> B["B. Controleer of je alles weet voor de fix"]
    
    B --> B1["Controleer:<br/>- CLAUDE.md files<br/>- README.md files<br/>- CLAUDE-AVISEO.md"]
    
    B1 --> B2{"Alle info<br/>aanwezig?"}
    
    B2 -->|Nee| B3["Vraag om hulp<br/>Geef aan wat ontbreekt"]
    B3 --> B1
    
    B2 -->|Ja| C["C. Bevestig:<br/>Ik heb alle vereiste informatie<br/>om de fix uit te voeren!"]
    
    C --> D["D. Start uitvoering van de fix"]
    
    D --> D1["Stap 1: Specificeer welke aanpassingen<br/>in codebase nodig zijn"]
    
    D1 --> D2["Stap 2: Maak gestructureerd plan<br/>met Todos"]
    
    D2 --> D3["Stap 3: Toon plan met Todos<br/>Vraag toestemming voor start"]
    
    D3 --> D3Check{"Toestemming<br/>ontvangen?"}
    
    D3Check -->|Nee| D3Wait["Wacht op toestemming"]
    D3Wait --> D3Check
    
    D3Check -->|Ja| D4["Stap 4: Toon lijst met Todos<br/>Start uitvoering"]
    
    D4 --> TodoLoop["Voor elke Todo:"]
    
    TodoLoop --> D5["Stap 5: Maak backup van files<br/>die gewijzigd worden"]
    
    D5 --> D6Execute["Voer Todo uit"]
    
    D6Execute --> D6["Stap 6: Maak samenvatting van gedane werk<br/>Werk Todo lijst bij<br/>Vraag toestemming voor volgende"]
    
    D6 --> D6Check{"Toestemming voor<br/>volgende Todo?"}
    
    D6Check -->|Nee| D6Wait["Wacht op toestemming"]
    D6Wait --> D6Check
    
    D6Check -->|Ja| AllDone{"Alle Todos<br/>afgewerkt?"}
    
    AllDone -->|Nee| TodoLoop
    
    AllDone -->|Ja| D7["Stap 7: Vraag toestemming om<br/>backups te verwijderen"]
    
    D7 --> D7Check{"Toestemming om<br/>backups te<br/>verwijderen?"}
    
    D7Check -->|Nee| KeepBackups["Behoud backups"]
    D7Check -->|Ja| DeleteBackups["Verwijder backups"]
    
    KeepBackups --> End([Fix voltooid])
    DeleteBackups --> End

Think hard!
