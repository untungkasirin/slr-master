```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#fff', 'edgeLabelBackground':'#fff', 'tertiaryColor': '#f4f4f4', 'mainBkg': '#fff', 'nodeBorder': '#333', 'clusterBkg': '#fff', 'clusterBorder': '#333', 'fontSize': '14px'}}}%%
graph LR
    %% DEFINISI SUB-GRAPH (KOTAK BESAR)
    %% PERBAIKAN: Menggunakan <br/> agar judul tidak terpotong
    subgraph KNOWing ["THE KNOWING:<br/>Financial Literacy"]
        direction TB
        K1[Knowledge]
        K2[Attitude]
        K3[Behavior]
    end

    subgraph DOing ["THE DOING:<br/>Cash Flow Management"]
        direction TB
        D1["<b>Budgeting Discipline</b><br/>Disiplin Anggaran"]
        D2["<b>Daily Cash Control</b><br/>Kontrol Kas Harian"]
        D3["<b>Debt Repayment</b><br/>Manajemen Utang"]
    end

    %% PERBAIKAN: Menggunakan <br/> agar judul tidak terpotong
    subgraph OUTcome ["OUTCOME:<br/>SME Performance"]
        direction TB
        O1["<b>Survival</b><br/>Kelangsungan Usaha"]
        O2["<b>Liquidity</b><br/>Likuiditas"]
    end

    subgraph TECH ["THE ENABLER:<br/>Digital Tech"]
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

    %% STYLING / PENGATURAN TAMPILAN YANG LEBIH KUAT
    %% Menggunakan !important untuk memaksa style diterapkan
    classDef box fill:#ffffff,stroke:#333,stroke-width:1.5px,rx:5,ry:5,text-align:center;
    classDef title font-weight:bold,text-align:center;
    
    %% MENERAPKAN STYLE KE KOTAK
    class K1,K2,K3,D1,D2,D3,O1,O2,T1,T2 box;
