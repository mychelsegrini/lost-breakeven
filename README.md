# Lost Breakeven: A Financial Game about Investment Funds for BTG Pactual

> **Note:** This is an English-language portfolio showcase for a project developed at the Institute of Technology and Leadership (Inteli), in São Paulo, Brazil. The original codebase, comments, and commit history are in Portuguese. This README provides a complete overview of the project and my specific contributions.
>
> The original (locked) group repository can be viewed for reference [here](https://github.com/InteliProjects/2025-1A-T16-IN01-G03).

---

## 🚀 Project Overview

Lost Breakeven is a Minimum Viable Product (MVP) of an educational game developed for **BTG Pactual**, the largest investment bank in Latin America. The project's goal was to create an engaging, interactive platform to teach fundamental concepts about investment funds for incoming analysts in onboarding.

### 📸 Visuals

![Gameplay Demo](https://github.com/mychelsegrini/lost-breakeven/blob/main/final.gif)

| Game Start Screen | In-Game Quest |
| :---: | :---: |
| ![](https://github.com/mychelsegrini/lost-breakeven/blob/main/mainMenu.png) | ![](https://github.com/mychelsegrini/lost-breakeven/blob/main/cofre.png)|

---

## 🛠️ Tech Stack

* **Game Engine:** [Phaser.js](https://phaser.io/) (A fast, free, and fun open-source HTML5 game framework)
* **Programming Language:** JavaScript
* **Development Tools:** VSCode, Git & GitHub
* **Methodology:** Scrum

---

## 🎯 My Role: Team Lead & Game Developer

As Scrum Master of an 8-person student development team, I was responsible for the technical architecture, game story, and the successful execution of the project, delivering the final MVP within a 10-week timeframe.

### Key Contributions:

* **Project Architecture:** Designed the foundational structure of the game, including game story, scene management, player state, and the main game loop, ensuring a scalable base for future development.
* **Core Gameplay Mechanics:** Personally architected and implemented key gameplay features using JavaScript and Phaser.js, including:
    * Player character movement and collision detection.
    * The NPC interaction system for delivering quests and financial tips.
    * Mathematical modelling for animation.
    * Dialogue system.
    * The logic for triggering and completing in-game educational objectives.
    * Sound implementation.

* **Agile Project Management:** Led the team using the Scrum methodology. I organized sprints, managed the task backlog, and facilitated daily stand-ups to ensure we met our deadlines and delivered a high-quality product to our partner, BTG Pactual.

Here is an illustrative snippet of the type of logic I was responsible for, handling an animation of three books flying in the final interaction with the game boss using polar coordinates:

```javascript
// Simplified example of player-NPC interaction logic
//Creates NPC's images
    this.adalberto = this.add
      .image(500, 900, "adalberto")
      .setScale(3.9)
      .setFlipX(true)
      .setVisible(false);
    this.finalAdalberto = this.add
      .image(1000, config.height / 2 - 200, "finalAdalberto")
      .setScale(4)
      .setVisible(false);

    //Creates Books Images
    this.diary = [];
    this.diary[0] = this.add
      .image(
        this.finalAdalberto.x + 200 * Math.sin(this.theta),
        this.finalAdalberto.y - 200 * Math.cos(this.theta),
        "diary1"
      )
      .setScale(2)
      .setVisible(false);
    this.diary[1] = this.add
      .image(
        this.finalAdalberto.x + 200 * Math.sin(this.theta + (2 * Math.PI) / 3),
        this.finalAdalberto.y - 200 * Math.cos(this.theta + (2 * Math.PI) / 3),
        "diary2"
      )
      .setScale(2)
      .setVisible(false);
    this.diary[2] = this.add
      .image(
        this.finalAdalberto.x + 200 * Math.sin(this.theta + (4 * Math.PI) / 3),
        this.finalAdalberto.y - 200 * Math.cos(this.theta + (4 * Math.PI) / 3),
        "diary3"
      )
      .setScale(2)
      .setVisible(false);
