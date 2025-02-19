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

    classDef default fill:#f9f,stroke:#333,stroke-width:2px;
    classDef section fill:#bbf,stroke:#333,stroke-width:2px;
    class NMAP,FirewallIDS,ServiceVersion,OSDetection,ScriptScan section
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
