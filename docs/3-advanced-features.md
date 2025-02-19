# Fonctionnalités Avancées NMAP

```mermaid
graph TB
    NMAP[NMAP]
    
    subgraph Evasion
    NMAP --> FirewallIDS[Evasion]
    FirewallIDS --> F1[f: Fragmentation]
    FirewallIDS --> F2[D: Leurre]
    FirewallIDS --> F3[S: Source IP Spoof]
    FirewallIDS --> F4[g: Source Port Spoof]
    end
    
    subgraph Versions
    NMAP --> ServiceVersion[Versions]
    ServiceVersion --> V1[sV: Version Scan]
    ServiceVersion --> V2[version-light: Scan léger]
    ServiceVersion --> V3[version-all: Scan intensif]
    end
    
    subgraph OS
    NMAP --> OSDetection[OS]
    OSDetection --> OS1[O: OS Detection]
    OSDetection --> OS2[osscan-guess: Detection agressive]
    end
    
    subgraph Scripts
    NMAP --> ScriptScan[NSE]
    ScriptScan --> SC1[sC: Scripts par défaut]
    ScriptScan --> SC2[script: Scripts spécifiques]
    ScriptScan --> SC3[script-args: Arguments]
    end

    classDef default fill:#e3f2fd,stroke:#2196f3,stroke-width:2px,color:#000;
    classDef section fill:#bbdefb,stroke:#1976d2,stroke-width:2px,color:#000;
    classDef root fill:#0d47a1,stroke:#002171,stroke-width:4px,color:#fff;
    class NMAP root;
    class FirewallIDS,ServiceVersion,OSDetection,ScriptScan section;
```

## Evasion de Firewall/IDS
- `f` : Fragmentation des paquets
- `D` : Utilisation de leurres
- `S` : Usurpation d'IP source
- `g` : Usurpation de port source

## Détection de Version
- `sV` : Scan de version standard
- `version-light` : Scan de version rapide
- `version-all` : Scan de version complet

## Détection de Système d'Exploitation
- `O` : Détection d'OS
- `osscan-guess` : Détection agressive

## Scripts NSE
- `sC` : Scripts par défaut
- `script` : Scripts personnalisés
- `script-args` : Arguments de scripts
