# Techniques de Scan NMAP

```mermaid
graph TB
    NMAP[NMAP]
    
    subgraph Types de Scan
    NMAP --> ScanTech[Types de Scan]
    ScanTech --> S1[sS: TCP SYN Scan]
    ScanTech --> S2[sT: TCP Connect Scan]
    ScanTech --> S3[sU: UDP Scan]
    ScanTech --> S4[sA: TCP ACK Scan]
    end
    
    subgraph Découverte d'Hôtes
    NMAP --> HostDisc[Découverte]
    HostDisc --> H1[Pn: Skip discovery]
    HostDisc --> H2[PS: TCP SYN Ping]
    HostDisc --> H3[PA: TCP ACK Ping]
    HostDisc --> H4[PU: UDP Ping]
    end
    
    subgraph Ports
    NMAP --> PortSpec[Ports]
    PortSpec --> P1[p: Ports spécifiques]
    PortSpec --> P2[F: Fast Scan]
    PortSpec --> P3[r: Scan séquentiel]
    end

    classDef default fill:#e3f2fd,stroke:#2196f3,stroke-width:2px,color:#000;
    classDef section fill:#bbdefb,stroke:#1976d2,stroke-width:2px,color:#000;
    classDef root fill:#0d47a1,stroke:#002171,stroke-width:4px,color:#fff;
    class NMAP root;
    class ScanTech,HostDisc,PortSpec section;
```

## Types de Scan
- `sS` : TCP SYN Scan (furtif)
- `sT` : TCP Connect Scan (complet)
- `sU` : UDP Scan
- `sA` : TCP ACK Scan

## Découverte d'Hôtes
- `Pn` : Ne pas faire de ping
- `PS` : TCP SYN Ping
- `PA` : TCP ACK Ping
- `PU` : UDP Ping

## Spécification des Ports
- `p` : Sélection de ports spécifiques
- `F` : Scan rapide
- `r` : Scan séquentiel
