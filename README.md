```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#fff', 'edgeLabelBackground':'#fff', 'tertiaryColor': '#f4f4f4', 'mainBkg': '#fff', 'nodeBorder': '#333', 'clusterBkg': '#fff', 'clusterBorder': '#333', 'fontSize': '16px', 'fontFamily': 'arial'}}}%%
graph LR
    %% --- KOTAK 1: THE KNOWING ---
    %% Judul tidak akan terpotong karena isi kotaknya (Financial Knowledge) sekarang sudah panjang
    subgraph KNOWing ["THE KNOWING:<br/>Financial Literacy"]
        direction TB
        K1["Financial Knowledge"]
        K2["Financial Attitude"]
        K3["Financial Behavior"]
    end

    %% --- KOTAK 2: THE DOING ---
    subgraph DOing ["THE DOING:<br/>Cash Flow Management"]
        direction TB
        D1["<b>Budgeting Discipline</b><br/>Disiplin Anggaran"]
        D2["<b>Daily Cash Control</b><br/>Kontrol Kas Harian"]
        D3["<b>Debt Repayment</b><br/>Manajemen Utang"]
    end

    %% --- KOTAK 3: OUTCOME ---
    subgraph OUTcome ["OUTCOME:<br/>SME Performance"]
        direction TB
        O1["Business Survival"]
        O2["Business Liquidity"]
    end

    %% --- KOTAK 4: ENABLER ---
    subgraph TECH ["THE ENABLER:<br/>Digital Tech"]
        direction LR
        T1["Fintech Applications"]
        T2["Digital Payments"]
    end

    %% HUBUNGAN ANTAR VARIABEL
    K1 & K2 & K3 --> DOing
    D1 & D2 & D3 --> OUTcome
    
    %% HUBUNGAN ENABLER
    TECH -.-> KNOWing
    TECH -.-> DOing

    %% STYLING SIMPLE & BERSIH
    classDef box fill:#ffffff,stroke:#333,stroke-width:1.5px,rx:5,ry:5,text-align:center,min-width:150px;
    classDef title font-weight:bold,text-align:center,font-size:16px;
    
    class K1,K2,K3,D1,D2,D3,O1,O2,T1,T2 box;
