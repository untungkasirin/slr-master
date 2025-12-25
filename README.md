```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#fff', 'edgeLabelBackground':'#fff', 'tertiaryColor': '#f4f4f4', 'mainBkg': '#fff', 'nodeBorder': '#333', 'clusterBkg': '#fff', 'clusterBorder': '#333', 'fontSize': '16px', 'fontFamily': 'arial'}}}%%
graph LR
    %% DEFINISI SUB-GRAPH
    %% TRICK: Menggunakan <br/> untuk judul
    subgraph KNOWing ["THE KNOWING:<br/>Financial Literacy"]
        direction TB
        %% TRICK: Menambah spasi &nbsp; agar kotak melebar & judul tidak terpotong
        K1["&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Knowledge&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"]
        K2["&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Attitude&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"]
        K3["&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Behavior&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"]
    end

    subgraph DOing ["THE DOING:<br/>Cash Flow Management"]
        direction TB
        D1["<b>Budgeting Discipline</b><br/>Disiplin Anggaran"]
        D2["<b>Daily Cash Control</b><br/>Kontrol Kas Harian"]
        D3["<b>Debt Repayment</b><br/>Manajemen Utang"]
    end

    subgraph OUTcome ["OUTCOME:<br/>SME Performance"]
        direction TB
        O1["&nbsp;&nbsp;<b>Survival</b><br/>Kelangsungan&nbsp;&nbsp;"]
        O2["&nbsp;&nbsp;&nbsp;<b>Liquidity</b><br/>Likuiditas&nbsp;&nbsp;&nbsp;"]
    end

    subgraph TECH ["THE ENABLER:<br/>Digital Tech"]
        direction LR
        T1["&nbsp;&nbsp;Fintech Apps&nbsp;&nbsp;"]
        T2["Digital Payments"]
    end

    %% HUBUNGAN ANTAR VARIABEL
    K1 & K2 & K3 --> DOing
    D1 & D2 & D3 --> OUTcome
    
    %% HUBUNGAN ENABLER
    TECH -.-> KNOWing
    TECH -.-> DOing

    %% STYLING
    classDef box fill:#ffffff,stroke:#333,stroke-width:1.5px,rx:5,ry:5,text-align:center;
    classDef title font-weight:bold,text-align:center,font-size:16px;
    
    class K1,K2,K3,D1,D2,D3,O1,O2,T1,T2 box;
