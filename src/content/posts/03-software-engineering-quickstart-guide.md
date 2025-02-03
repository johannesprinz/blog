---
title: "Software Engineering Quick Start Guide"
date: 2023-11-22T23:56:09Z
draft: false
tags:
  - Getting Started
  - Software Engineering
categories:
  - HowTo
---

Below you will find some resources that define my engineering ethos. These are
categorised into the three main pillars of every change I make.

1.  The Why ( Values, Documentation, Commit messages, Comments )
2.  The What ( Principles, Documentation, Tests )
3.  The How ( Process, Architecture, Code, Tools )

### Why

- Documentation
  - [Diataxis](https://diataxis.fr/) a great giode for starting to document in code
    - [Tutorials](https://diataxis.fr/tutorials/) for learning.
    - [How to guides](https://diataxis.fr/how-to-guides/) for reaching goals.
    - [Explanations](https://diataxis.fr/explanation/) to aid understanding.
    - [Reference](https://diataxis.fr/reference/) for detailed information.
  - [C4 Model](https://c4model.com/) a great way to declaratively create the core system diagrams
  - [Arc 42 templates](https://arc42.org/overview) a base structure on how to document a software system, can be as simple as as a single page or complext as you need it to be.
  - [Kepp a change log](https://keepachangelog.com/en/1.1.0/) track your changes in human readable form.
  - [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) track your changes in detail.
  - [Documenting Architecture Decisions](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions) track your decisions in human readable form.
  - [Mermaid Markdown](https://mermaid.js.org/#/) free form declaritive diagramming.

### What

- [Test Driven Development (TDD)](https://en.wikipedia.org/wiki/Test-driven_development)
  - Test first: Red, Green, Refactor
  - Test naming: Given_When_Then
  - Structure: Arrange, Act, Assert
  - Process:
    - Start with degenerate test cases first.
    - As the tests get more specific, the code becomes more generic.
  - [Katas](http://codekata.com/):
    - [Uncle Bobs TDD Kata](https://www.youtube.com/watch?v=kScFczWbwRM)
    - [Gilding the Rose](https://youtu.be/kTcDBYCpj7Q)
  - Two TDD styles,
    [London vs Chicago](https://devlead.io/DevTips/LondonVsChicago) more
    concretely covered by Sandro Mancuso below
  - [Uncle bobs response to TDD Harms Architecture](http://blog.cleancoder.com/uncle-bob/2017/03/03/TDD-Harms-Architecture.html)
  - [Interesting debate](https://www.youtube.com/watch?v=KtHQGs3zFAM)
  - [Why TDD sometimes feels hard](https://www.youtube.com/watch?v=UWtEVKVPBQ0)
  - [TDD for those who don't need it](https://www.youtube.com/watch?v=a6oP24CSdUg)

### How

- [Agile manifesto](https://agilemanifesto.org/)
  - The values and principles are key to understanding no matter what agile
    methodology is used.
- Clean Architecture
  - [Architecture 101](https://hackernoon.com/how-to-design-a-web-application-software-architecture-101-eecy36o5)
  - [Jason Taylors - Clean Architecture repo](https://github.com/jasontaylordev/CleanArchitecture)
    and [here it is Explained](https://www.youtube.com/watch?v=YiVqwoFMieg)
  - [Here is Steve Smiths version](https://github.com/ardalis/CleanArchitecture)
    for a comparison
  - [Clean Architecture and Design by Robert C. Martin (Uncle Bob)](https://www.youtube.com/watch?v=2dKZ-dWaCiU)
  - [Linking TDD and Clean Architecture by Sandro Mancuso](https://www.youtube.com/watch?v=KyFVA4Spcgg).
    Does TDD Really Lead to Good Design?
- Clean Code
  - [Clean code video series](https://cleancoders.com/library/all)
  - [SOLID Principles](https://en.wikipedia.org/wiki/SOLID)
  - [CUPID](https://dannorth.net/2022/02/10/cupid-for-joyful-coding/)
  - [Object Callisthenics](https://williamdurand.fr/2013/06/03/object-calisthenics/)
  - [Code Smells](https://refactoring.guru/refactoring/smells)
    - [Refactoring](https://en.wikipedia.org/wiki/Code_refactoring)
    - [Refactoring Techniques](https://refactoring.guru/refactoring/techniques)
  - [The last programming language](https://www.youtube.com/watch?v=P2yr-3F6PQo)

### Must Watch Software Talks For Software Engineers

- Christin Gorman “Gordon Ramsay Doesn’t Use Cake Mixes” ➡️
  <https://vimeo.com/28885655>
- Bryan Liles “Test all the f\*^&ing time” ➡️ <https://youtu.be/iwUR0kOVNs8>
- Gojko Adzic “Make Impacts, not Software” ➡️ <https://youtu.be/GnK_n9Udhhs>
- Jeff Patton “User Story Mapping” ➡️ <https://youtu.be/AzBuohuOU6g>
- Michael Nygard "Uncoupling" ➡️ <https://youtu.be/mAw4ygX1c-4>
- Gregor Hohpe “Enterprise Architecture = Architecting the Enterprise?” ➡️
  <https://youtu.be/DdJNLeYldUs>
- Eric Evans "Tackling the complexity at the heart of software" ➡️
  <https://youtu.be/dnUFEg68ESM>
- Jim Webber, "The Present and Future of Native Graph Technology" ➡️
  <https://youtu.be/_CQehnb6A6o>
- Jez Humble, “CD sounds great, but can’t work here” ➡️
  <https://youtu.be/IvWr29afDF8>
- Anita Sengupta, “The future of Mars exploration" ➡️
  <https://youtu.be/iuzZYzns-Yg>
- Hanna Fry, “How to be human in the age of the machine” ➡️
  <https://youtu.be/Rzhpf1Ai7Z4>
- [Better Coding playlist](https://www.youtube.com/playlist?list=PLbB0DkO_4qsTM3LAO-1d7lkvY2PtRyEpQ)
