# Commandes de Base NMAP

```mermaid
graph TB
    NMAP[NMAP]
    
    subgraph Commandes Diverses
    NMAP --> Misc[Divers]
    Misc --> M1[help: Afficher l'aide]
    Misc --> M2[v: Augmenter verbosité]
    Misc --> M3[privileged: Mode privilégié]
    end
    
    subgraph Options de Sortie
    NMAP --> Output[Sortie]
    Output --> O1[oN: Output normal]
    Output --> O2[oX: Output XML]
    Output --> O3[oG: Output Grepable]
    Output --> O4[v: Verbosité]
    end

    classDef default fill:#e3f2fd,stroke:#2196f3,stroke-width:2px,color:#000;
    classDef section fill:#bbdefb,stroke:#1976d2,stroke-width:2px,color:#000;
    classDef root fill:#0d47a1,stroke:#002171,stroke-width:4px,color:#fff;
    class NMAP root;
    class Misc,Output section
```

## Commandes Diverses
- `help` : Afficher la page d'aide
- `v` : Augmenter le niveau de verbosité
- `privileged` : Mode privilégié

## Options de Sortie
- `oN` : Format de sortie normal (texte)
- `oX` : Format XML
- `oG` : Format Grepable
- `v` : Contrôle de la verbosité
