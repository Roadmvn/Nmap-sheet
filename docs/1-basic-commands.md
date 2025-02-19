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

    classDef default fill:#f9f,stroke:#333,stroke-width:2px;
    classDef section fill:#bbf,stroke:#333,stroke-width:2px;
    class NMAP,Misc,Output section
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
