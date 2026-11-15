# Unity / C# — Tabletop RPG companion

[← Back to GitHub profile](../README.md)

**Personal project · In development · Application source not public**

## Overview

I am developing a **2D tabletop role-playing companion application** with Unity and C#. The aim is to bring together game-session tooling, synchronized interaction between participants and persistent application data.

This is an **unofficial fan-made companion project**, not an official publisher product or an affiliated game. The application is not offered here as a playable public release.

## Technology

| Area | Technology | Purpose |
| --- | --- | --- |
| Application | Unity 6, C# | 2D application and interaction |
| Multiplayer | Unity Netcode for GameObjects | Networking and synchronized game state |
| Data | Firebase / Cloud Firestore | Persistent information |
| Testing | NUnit | Automated testing of selected logic |

## Engineering focus

### Multiplayer state

One challenge is deciding which state belongs to a participant's local interface and which changes need to be shared with the rest of a session. Using Netcode for GameObjects means accounting for network ownership, synchronization and failure modes rather than assuming a single local user.

### Data and application structure

The project combines Unity gameplay/UI code with persistent records. Organizing responsibilities and keeping data operations separate from presentation makes changes easier to test and maintain.

### Iterative implementation

This is ongoing development. The technology choices above reflect the project's implementation direction; **not all features are independently verified here, and no shipped network or production reliability claims are made**.

## Public evidence

- [Projet40K — public graphics repository](https://github.com/matheovitali/Projet40K): currently **graphics/assets only**, not the Unity application source.
- A build, gameplay video and screenshots of the actual Unity application have **not yet been published**.
- The private project source would need a review for third-party content, licenses, credentials and repository history before any code release.

## Planned portfolio media

A useful future demonstration would show a **sanitized session** with two locally controlled participants, a synchronized action, and data persistence, using placeholder content where rights are unclear. This describes a **demonstration to prepare**, not a video that is already available.

**Note on intellectual property:** references to tabletop games and any third-party artwork are used for project context only. No publisher endorsement, license to reuse images or affiliation is implied.
