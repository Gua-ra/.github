<h1 href="https://gua.global/about" align="center">Gua</h1>

<p align="center">
  <img src="https://github.com/user-attachments/assets/00897e57-a32e-4cc8-b863-1ee2a091cb02" width="200"  />
</p>

<p align="center">
  <strong>Comunicação descentralizada, segura e livre</strong><br/>
  <em>Decentralized, secure and free communication</em>
</p>

<p align="center">
  <a href="https://matrix.org"><img alt="Built on Matrix" src="https://img.shields.io/badge/built%20on-Matrix-0DBD8B?logo=matrix&logoColor=white"/></a>
  <img alt="Status: prototype" src="https://img.shields.io/badge/status-prototype-orange"/>
  <img alt="Open source" src="https://img.shields.io/badge/open%20source-yes-blue"/>
</p>

![](https://github.com/user-attachments/assets/565e1084-f0f7-483f-af31-b1ad5b45aaa3)


---
<div align="center">
    <h3><a href="https://gua.global/about">Learn more about Gua</a></b>
</div>

<br>

Gua is a **prototype of a private, decentralized, federated messenger** built on the open [Matrix protocol](https://matrix.org). The idea is simple: chatting should feel as easy as in any modern app, phone sign-in, finding your friends, end-to-end encryption, no ads, but in a **descentralized way**, without a single big-tech company owning the whole network.

It works like a normal modern messenger. Behind the scenes, it's something different.

---

<p align="center">
  <img src="./assets/guara-wolf.webp" alt="Lobo-guará — the maned wolf of Brazil - Photographer: Kathrin Mezger https://www.flickr.com/photos/26094756@N04/10542455354/" width="300"/>
</p>

<p align="center"><em>Named after the <strong>lobo-guará</strong>, the maned wolf of Brazil. An animal that roams long distances, lives in no pack, and answers to no owner</em></p>

---

<div align="center">
    <h3>Why Gua exists</h3>
</div>

Most of our conversations now live inside closed platforms, where one company controls the app, the servers, the rules, the code and your data. That creates dependency and fragility: the platform can change the rules overnight, mine your information to train AI models, block accounts, or shut a service down, and you have little real control.

Open source alone doesn't fix this. An app can have open code and still run on a **centralized network** where accounts, contact discovery, routing and operation all flow through infrastructure owned by one organization (e.g. [Signal](signal.org)). Better than a closed commercial platform, but still a single center of control.

Gua asks a different question: **what if you had a simple, modern-messenger experience — open code, end-to-end encryption — on a network that doesn't need to belong to any single company, foundation or provider?**

The vision is an open foundation for secure communication between people, communities, organizations, universities, local governments and institutions that need **digital sovereignty**, without giving up a simple experience for the everyday user. Gua is an open, federated, secure network: easy enough that people never have to think about it, and open enough that institutions can take part without handing all control to a central platform.

<div align="center">
    <h3>How the federation works
</h3>
</div>

Different servers, run by universities, carriers and institutions, take part in the same network. The Gua Resolver verifies which servers are trusted, keeping the network open and safe at once.

```mermaid
graph TB
  subgraph NET["🐺 GUA NETWORK"]
    direction TB
    R(["🛡️ Gua Resolver<br/>verifies and routes"])
    INST(["🏛️ Institutional<br/>City Hall"])
    UNI(["🎓 Public server<br/>University"])
    CAR(["📡 Public server<br/>Carrier"])

    R -. verifies .-> INST
    R -. verifies .-> UNI
    R -. verifies .-> CAR

    INST <--> UNI
    UNI <--> CAR
    INST <--> CAR

    Dan(["💻 Dan"]) --- INST
    Carol(["📱 Carol"]) --- INST
    Ana(["📱 Ana"]) --- UNI
    Jean(["💻 Jean"]) --- UNI
    Lia(["📱 Lia"]) --- CAR
    Bruno(["💻 Bruno"]) --- CAR
  end

  classDef res fill:#e6f7f8,stroke:#0d9aa6,stroke-width:2px,color:#0a6f78;
  classDef inst fill:#e8f7ef,stroke:#1f9d5b,stroke-width:2px,color:#0c603a;
  classDef pub fill:#fdf1e3,stroke:#e08a2b,stroke-width:2px,color:#9a5916;
  classDef user fill:#ffffff,stroke:#9fb4a8,stroke-width:1px,color:#3c5a49;

  class R res;
  class INST inst;
  class UNI,CAR pub;
  class Dan,Carol,Ana,Jean,Lia,Bruno user;

  style NET fill:#fbfdfb,stroke:#cfe6d6,stroke-width:2px,stroke-dasharray:6 5;
```

In a **centralized** app, everyone depends on the same backend. In a **federated** network, different servers, each run by a trusted organization, community or institution, take part in the same network, the way email lets accounts on different providers still write to each other, end-to-end encrypted.

Gua does **not** open the network to any unknown server. The goal is a *secure, verifiable federation*. Its "front door" is a component called the [**Gua Resolver**](https://github.com/Gua-ra/gua-resolver): before you log in, the app queries it to find where an account should sign in, and it holds a signed list of trusted servers. The resolver verifies and serves that list; which servers are trusted is decided by the federation's published rules, not by the resolver itself. It helps answer three questions:

1. **Which server** does this account belong to?
2. **Is that server** part of the trusted Gua network?
3. **Were the rules** that decide where new accounts are created published in a verifiable way?

The result: decentralization without complexity, independence combined with trust.

For the design behind this, with an honest line between what is built today and what is still the target, read the [Gua identity and federation guide](https://github.com/Gua-ra/gua-resolver/blob/main/docs/architecture/gua-identity-and-federation.md).


## Project / ecosystem

All of Gua is open source, like the rest of the Matrix ecosystem. Everything lives under [**github.com/Gua-ra**](https://github.com/Gua-ra).

| Repository | What it is |
| --- | --- |
| [**gua-resolver**](https://github.com/Gua-ra/gua-resolver) | The federation "front door": resolves which trusted server an account belongs to and holds the signed list of trusted servers. |
| [**gua-web**](https://github.com/Gua-ra/gua-web) | Web client. |
| [**gua-ios**](https://github.com/Gua-ra/gua-ios) | iOS client. |
| [**identity-service**](https://github.com/Gua-ra/identity-service) | Sign-up, contact discovery and sign-in backend used by the prototype today. |
| [**gua-auth-service**](https://github.com/Gua-ra/gua-auth-service) | Authentication service. |
| [**gua-idp-web**](https://github.com/Gua-ra/gua-idp-web) | Sign-in / identity web UI. |
| [**gua-branding**](https://github.com/Gua-ra/gua-branding) | Brand assets. |

**How it fits together:**

- **Clients** — `gua-web`, `gua-ios`:  the apps people use.
- **Federation & trust**: `gua-resolver`: resolves accounts to servers and verifies which servers are trusted.
- **Identity & sign-in**: `identity-service`, `gua-auth-service`, `gua-idp-web`: account sign-up, contact discovery, authentication and the sign-in UI, as the prototype runs today. In the target design, each server owns authentication for its own accounts.
- **Brand & deployment**: `gua-branding`, `gua-deploy`.

## Status

Gua is at the **prototype** stage. Features may change, break or be incomplete, and it is **not yet meant to be critical infrastructure**. Personal use is designed to stay **free**.

## Contact

- **General contact:** [contact@gua.global](mailto:contact@gua.global)

---

<p align="center"><em>Built on the open <a href="https://matrix.org">Matrix protocol</a>. Free, independent, owned by no one. 🐺</em></p>
