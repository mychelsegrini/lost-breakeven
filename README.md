# FinanCity: A Financial Literacy Game for BTG Pactual

> **Note:** This is an English-language portfolio showcase for a project developed at the Institute of Technology and Leadership (Inteli) in Brazil. The original codebase, comments, and commit history are in Portuguese. This README provides a complete overview of the project and my specific contributions.
>
> The original (locked) group repository can be viewed for reference [here](https://github.com/InteliProjects/2025-1A-T16-IN01-G03).

---

## 🚀 Project Overview

Lost Breakeven is a Minimum Viable Product (MVP) of an educational game developed for **BTG Pactual**, the largest investment bank in Latin America. The project's goal was to create an engaging, interactive platform to teach fundamental concepts about investment funds for incoming analysts in onboarding.

### 📸 Visuals

*[INSERT A GIF OF GAMEPLAY HERE. This is the most important element! You can use a free tool like Giphy Capture or ScreenToGif to record your screen.]*

| Game Start Screen | In-Game Quest |
| :---: | :---: |
| *[INSERT SCREENSHOT OF THE MAIN MENU HERE]* | *[INSERT SCREENSHOT OF A PLAYER INTERACTING WITH AN NPC OR OBJECTIVE HERE]* |

---

## 🛠️ Tech Stack

* **Game Engine:** [Phaser.js](https://phaser.io/) (A fast, free, and fun open-source HTML5 game framework)
* **Programming Language:** JavaScript
* **Development Tools:** VSCode, Git & GitHub
* **Methodology:** Scrum

---

## 🎯 My Role: Team Lead & Game Developer

As the leader of an 8-person student development team, I was responsible for both the technical architecture and the successful execution of the project, delivering the final MVP within a 10-week timeframe.

### Key Contributions:

* **Project Architecture:** Designed the foundational structure of the game, including scene management, player state, and the main game loop, ensuring a scalable base for future development.
* **Core Gameplay Mechanics:** Personally architected and implemented key gameplay features using JavaScript and Phaser.js, including:
    * Player character movement and collision detection.
    * The NPC interaction system for delivering quests and financial tips.
    * The logic for triggering and completing in-game educational objectives.
* **Agile Project Management:** Led the team using the Scrum methodology. I organized sprints, managed the task backlog, and facilitated daily stand-ups to ensure we met our deadlines and delivered a high-quality product to our client, BTG Pactual.

Here is an illustrative snippet of the type of logic I was responsible for, handling player interaction with a quest-giving NPC:

```javascript
// Simplified example of player-NPC interaction logic
function onPlayerContact(player, npc) {
    // Check if the NPC has a quest and the player hasn't completed it
    if (npc.hasQuest && !player.quests.completed[npc.questId]) {
        // Stop player movement and trigger the dialogue UI
        player.body.stop();
        dialogueManager.startDialogue(npc.dialogueTree);
    }
}
