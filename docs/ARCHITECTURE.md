# Public Architecture Overview

This document describes the public, high-level structure of ZeroPlay Games. It intentionally excludes production implementation details, secrets, deployment credentials, private analytics identifiers, and game runtime source.

## Content model

```text
Home
├── Popular Games
├── Category highlights
│
├── All Games
│   └── Full catalog grouped by category
│
├── 9 Category pages
│   └── Game inventory by broad category
│
├── 9 Gameplay Topic hubs
│   └── Game discovery by mechanic
│
└── 100 Game pages
    ├── Play entry
    ├── Objective
    ├── Controls
    ├── How to play
    ├── Rules
    ├── Tips
    ├── FAQ
    └── Related game discovery
```

## Category layer

The catalog is organized into:

- Action
- Arcade
- Casual
- Idle
- Puzzle
- Racing
- Shooting
- Sports
- Strategy

## Gameplay topic layer

Current gameplay hubs include:

- Tap Games
- Merge Games
- Defense Games
- Memory Games
- Reaction Games
- Number Games
- Word Games
- Classic Games
- Idle & Clicker Games

A game may belong to more than one gameplay topic while retaining one canonical game page.

## Language structure

The public website maintains independent route trees for:

- English
- Simplified Chinese
- Traditional Chinese
- Spanish

Equivalent pages are connected through canonical/hreflang metadata on the production site.

## Indexing model

Public search landing pages include:

- Home
- All Games
- Category pages
- Gameplay Topic hubs
- Individual Game pages
- About/legal pages

Search utility pages and raw game runtime files are not intended to be independent search landing pages.

## Discovery model

The product is designed around:

```text
Search / Direct / Social
        ↓
     Game A
        ↓
Same-category recommendations
        +
Cross-category discovery
        ↓
     Game B
        ↓
     Game C
```

The long-term product goal is not only page views, but more successful game starts and more games played per session.
