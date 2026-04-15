# RCBox Network Topologies

RCBox is a Raspberry Pi–powered micro server and Wi-Fi hotspot that serves
static content offline and hosts secure messaging and public chat.

## 1. Standalone Offline — Direct Wi-Fi Clients

A single RCBox acts as an access point; clients associate directly to its
Wi-Fi radio. No internet, no upstream — fully self-contained.

```mermaid
flowchart TB
    subgraph RCBox["RCBox (Raspberry Pi)"]
        AP["Wi-Fi Access Point"]
        WEB["Static Content Server"]
        MSG["Secure Messaging"]
        CHAT["Public Chat Room"]
        AP --- WEB
        AP --- MSG
        AP --- CHAT
    end

    LAPTOP["Laptop"]
    PHONE1["Phone"]
    PHONE2["Phone"]
    TABLET["Tablet"]

    LAPTOP -. "Wi-Fi" .-> AP
    PHONE1 -. "Wi-Fi" .-> AP
    PHONE2 -. "Wi-Fi" .-> AP
    TABLET -. "Wi-Fi" .-> AP
```

## 2. Multiple RCBoxes on a Wired LAN

Several RCBoxes are joined by Ethernet and share data peer-to-peer across
the wired backbone. Each RCBox continues to serve its own Wi-Fi clients.

```mermaid
flowchart TB
    SWITCH["Ethernet Switch / Wired LAN"]

    subgraph BOX1["RCBox #1"]
        AP1["Wi-Fi AP"]
        SVC1["Content / Msg / Chat"]
        ETH1["Ethernet"]
        AP1 --- SVC1
        SVC1 --- ETH1
    end

    subgraph BOX2["RCBox #2"]
        AP2["Wi-Fi AP"]
        SVC2["Content / Msg / Chat"]
        ETH2["Ethernet"]
        AP2 --- SVC2
        SVC2 --- ETH2
    end

    subgraph BOX3["RCBox #3"]
        AP3["Wi-Fi AP"]
        SVC3["Content / Msg / Chat"]
        ETH3["Ethernet"]
        AP3 --- SVC3
        SVC3 --- ETH3
    end

    ETH1 --- SWITCH
    ETH2 --- SWITCH
    ETH3 --- SWITCH

    C1["Laptop"] -. "Wi-Fi" .-> AP1
    C2["Phone"]  -. "Wi-Fi" .-> AP1
    C3["Phone"]  -. "Wi-Fi" .-> AP2
    C4["Tablet"] -. "Wi-Fi" .-> AP2
    C5["Laptop"] -. "Wi-Fi" .-> AP3

    SVC1 <== "peer sync" ==> SVC2
    SVC2 <== "peer sync" ==> SVC3
    SVC1 <== "peer sync" ==> SVC3
```

## 3. RCBox with Wi-Fi HaLow Extended Range

An RCBox uplinks to a Wi-Fi HaLow hub router. Remote endpoints reach the
hub via HaLow bridges — one bridging a client device, another bridging a
second RCBox at distance.

```mermaid
flowchart TB
    subgraph BOX1["RCBox #1 (primary)"]
        AP1["Wi-Fi AP (2.4/5 GHz)"]
        SVC1["Content / Msg / Chat"]
        AP1 --- SVC1
    end

    HUB["Wi-Fi HaLow Hub Router"]

    BR1["HaLow Bridge A"]
    BR2["HaLow Bridge B"]

    CLIENT["Remote Client (Laptop)"]

    subgraph BOX2["RCBox #2 (remote)"]
        AP2["Wi-Fi AP"]
        SVC2["Content / Msg / Chat"]
        AP2 --- SVC2
    end

    LOCAL1["Phone"] -. "Wi-Fi" .-> AP1
    LOCAL2["Laptop"] -. "Wi-Fi" .-> AP1

    BOX1 <== "Ethernet / Wi-Fi" ==> HUB
    HUB <-. "HaLow (long range)" .-> BR1
    HUB <-. "HaLow (long range)" .-> BR2

    BR1 --- CLIENT
    BR2 === BOX2

    LOCAL3["Phone"] -. "Wi-Fi" .-> AP2

    SVC1 <== "peer sync over HaLow" ==> SVC2
```

## 4. Opportunistic Mobile Mesh

A stationary RCBox anchors a location. Mobile RCBoxes — one mounted in a
bus, another on a motorcycle — carry data as they move, syncing
opportunistically whenever they come within Wi-Fi range of the base or
each other (a store-and-forward "sneakernet over Wi-Fi").

```mermaid
flowchart TB
    subgraph BASE["Stationary RCBox (fixed location)"]
        APB["Wi-Fi AP"]
        SVCB["Content / Msg / Chat"]
        STOREB[("Local Data Store")]
        APB --- SVCB
        SVCB --- STOREB
    end

    LC1["Local Phone"] -. "Wi-Fi" .-> APB
    LC2["Local Laptop"] -. "Wi-Fi" .-> APB

    subgraph BUS["Mobile RCBox — Bus"]
        APBUS["Wi-Fi AP"]
        SVCBUS["Content / Msg / Chat"]
        STOREBUS[("Local Data Store")]
        APBUS --- SVCBUS
        SVCBUS --- STOREBUS
    end

    PBUS1["Passenger Phone"] -. "Wi-Fi" .-> APBUS
    PBUS2["Passenger Phone"] -. "Wi-Fi" .-> APBUS

    subgraph MOTO["Mobile RCBox — Motorcycle"]
        APM["Wi-Fi AP"]
        SVCM["Content / Msg / Chat"]
        STOREM[("Local Data Store")]
        APM --- SVCM
        SVCM --- STOREM
    end

    RIDER["Rider Phone"] -. "Wi-Fi" .-> APM

    SVCB  <-. "sync when in range" .-> SVCBUS
    SVCB  <-. "sync when in range" .-> SVCM
    SVCBUS <-. "sync when in range" .-> SVCM
```

