```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#fff', 'edgeLabelBackground':'#fff', 'tertiaryColor': '#f4f4f4', 'mainBkg': '#fff', 'nodeBorder': '#333', 'clusterBkg': '#fff', 'clusterBorder': '#333'}}}%%
graph LR
    %% DEFINISI SUB-GRAPH (KOTAK BESAR)
    subgraph KNOWing [THE KNOWING: Financial Literacy]
        direction TB
        K1[Knowledge]
        K2[Attitude]
        K3[Behavior]
    end

    subgraph DOing [THE DOING: Cash Flow Management]
        direction TB
        D1[<b>Budgeting Discipline</b><br/>Disiplin Anggaran]
        D2[<b>Daily Cash Control</b><br/>Kontrol Kas Harian]
        D3[<b>Debt Repayment</b><br/>Manajemen Utang]
    end

    subgraph OUTcome [OUTCOME: SME Performance]
        direction TB
        O1[<b>Survival</b><br/>Kelangsungan Usaha]
        O2[<b>Liquidity</b><br/>Likuiditas]
    end

    subgraph TECH [THE ENABLER: Digital Tech]
        direction LR
        T1[Fintech Apps]
        T2[Digital Payments]
    end

    %% HUBUNGAN ANTAR VARIABEL (GARIS SOLID)
    K1 & K2 & K3 --> DOing
    D1 & D2 & D3 --> OUTcome
    
    %% HUBUNGAN ENABLER (GARIS PUTUS-PUTUS)
    TECH -.-> KNOWing
    TECH -.-> DOing

    %% STYLING / PENGATURAN TAMPILAN
    classDef box fill:#ffffff,stroke:#333,stroke-width:1.5px,rx:0,ry:0;
    classDef title fill:#f9f9f9,stroke:#333,stroke-width:1px,font-weight:bold,rx:0,ry:0;
    
    %% MENERAPKAN STYLE KE KOTAK
    class KNOWing,DOing,OUTcome,TECH title;
    class K1,K2,K3,D1,D2,D3,O1,O2,T1,T2 box;
