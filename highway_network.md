## 1. QUESTION 2 - DIRECTED GRAPH 

The directed graph represents the highway connections across major towns and cities in the Nairobi, Central Highlands, Rift Valley and Lake Victoria basin regions. 

```mermaid
flowchart TD 

    subgraph NAIROBI["NAIROBI REGION"]
        N[Nairobi]
        R[Ruiru]
        T[Thika]
        MM[Mai Mahiu]

        N <--> R
        R <--> T
        N <--> MM
    end

    subgraph CENTRAL["CENTRAL HIGHLANDS"]
        MU[Murang'a]
        S[Sagana]
        KA[Karatina]
        NY[Nyeri]
        NA[Nanyuki]
        EM[Embu]

        T <--> MU
        MU <--> S
        S <--> KA
        KA <--> NY
        NY <--> NA
        S <--> EM
    end

   subgraph RIFT["RIFT VALLEY"]
       NV[Naivasha]
       NK[Nakuru]
       MO[Molo]
       KE[Kericho]
       BO[Bomet]
       NR[Narok]
       NH[Nyahururu]

       MM <--> NV
       NV <--> NK
       NK <--> MO
       MO <--> KE
       NK <--> NH
       KE <--> BO
       BO <--> NR
    end       

    subgraph LAKE["LAKE VICTORIA BASIN"]
        KI[Kisumu]
        AH[Ahero]
        SO[Sondu]
        HB[Homa Bay]
        KS[Kisii]
        MI[Migori]

        KE <--> SO
        SO <--> KI
        KI <--> AH
        KI <--> HB
        HB <--> KS
        KS <--> MI
    end
```

## 2. GRAPH WITH ABSTRACTION


Abstraction simplifies the network by grouping the regions and removing unnecessary details. 

```mermaid
flowchart TD 
    A["KENYA HIGHWAY NETWORK"]

    A --> B["NAIROBI REGION"]
    A --> C["CENTRAL HIGHLANDS"]
    A --> D["RIFT VALLEY"]
    A --> E["LAKE VICTORIA BASIN"]

    B --> F[Nairobi]
    B --> G[Ruiru]
    B --> H[Thika]
    B --> I[Mai Mahiu]

    C --> J[Murang'a]
    C --> K[Sagana]
    C --> L[Karatina]
    C --> M[Nyeri]
    C --> N[Nanyuki]
    C --> O[Embu]

    D --> P[Naivasha]
    D --> Q[Nakuru]
    D --> R[Molo]
    D --> S[Kericho]
    D --> T[Bomet]
    D --> U[Narok]
    D --> V[Nyahururu]

    E --> W[Kisumu]
    E --> X[Ahero]
    E --> Y[Sondu]
    E --> Z[Homa Bay]
    E --> AA[Kisii]
    E --> AB[Migori]
```

## 3. SEARCH TREE EXAMPLE

Start: Nairobi.
End: Kisumu

```mermaid
flowchart TD 
    A["START: Nairobi"]
    A --> B[Mai Mahiu]
    B --> C[Naivasha]
    C --> D[Nakuru]

    D --> E[Molo]
    D --> F[Nyahururu]

    E --> G[Kericho]
    G --> H[Sondu]
    H --> I["GOAL: Kisumu"]

    G --> J[Bomet]
    J --> K[Narok]
``` 

