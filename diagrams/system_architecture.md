flowchart LR
  %% High-level architecture for a cloud-based financial services web app

  subgraph Internet["Internet"]
    C[Customer]
    A[Attacker]
  end

  subgraph Cloud["Cloud Environment"]
    subgraph App["Application Layer"]
      W[Web Application]
      Auth[Authentication Service<br/>(Password + MFA)]
    end

    subgraph Services["Service Layer"]
      API[API Layer]
      Tx[Transaction Engine]
    end

    subgraph Data["Data Layer"]
      DB[(Customer Database<br/>PII + Financial Data)]
    end

    subgraph Security["Security Controls"]
      IAM[Cloud IAM<br/>(Roles + Policies)]
      SIEM[Central Logging / SIEM]
    end

    TP[Third-Party Services<br/>(Email, SaaS)]
  end

  %% Legitimate flows
  C --> W
  W --> Auth
  W --> API
  API --> Tx
  Tx --> DB
  W --> TP

  %% Security control coverage
  IAM -. governs access .-> W
  IAM -. governs access .-> Auth
  IAM -. governs access .-> API
  IAM -. governs access .-> Tx
  IAM -. governs access .-> DB

  W -. logs .-> SIEM
  Auth -. logs .-> SIEM
  API -. logs .-> SIEM
  Tx -. logs .-> SIEM
  DB -. logs .-> SIEM

  %% Threat entry point (optional visual)
  A -. targets .-> W

