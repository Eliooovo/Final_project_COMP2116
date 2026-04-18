# COMP2116 Final Project: Arcane Lexicon (Wordle Game)

## Graphical Abstract
<img width="1024" height="816" alt="dcb501a3e37ffc227f1cb90a808efecc" src="https://github.com/user-attachments/assets/a38ec8a6-d211-4e0f-b2af-c7ada78f5ed2" />


*(Figure: The main interface of Arcane Lexicon, showcasing the retro pixel-art UI, the 4x4 game grid, the virtual keyboard, and the dynamic "Discovered Letters" hint panel on the right.)*

---

## Purpose of the software

### Which type of software development process is applied
This project adopted the **Agile Development Process**. The software was developed and refined gradually through multiple short iterations (Sprints).

### Why you chose this type (Waterfall vs. Agile)?
Compared to the traditional Waterfall model, Agile is significantly more suitable for this game project for the following reasons:
* **Rapid Feedback and Continuous Iteration:** Game development requires constant adjustments to user experience (UX) and difficulty balance. Agile allowed us to build the core spelling validation logic early on for rapid testing, and subsequently introduce the 6x6 Hard Mode and the dynamic "Discovered Letters" hint panel in later iterations.
* **Flexibility to Changing Requirements:** During development, we realized the need for a convenient testing and demonstration mechanism. Agile enabled us to seamlessly append a hidden "Developer Mode" (accessed via specific login credentials) to bypass level restrictions and view target words directly, which would be difficult to implement midway in a rigid Waterfall model.

### Possible usage of your software (i.e., target market)
* **Target Market:** English learners, word puzzle enthusiasts, and players seeking casual, brain-training web games.
* **Possible Usage:** Users can play directly via web browsers during their fragmented free time without downloading or installing any applications, thereby improving their English spelling, vocabulary, and logical deduction skills.

---

## Software development plan

### Development Process
The development lifecycle was divided into three main Sprints:
* **Sprint 1 (Core Logic):** Set up the foundational HTML/CSS layout, implemented the core Wordle algorithm driven by Vanilla JS (Green, Yellow, Grey state validation logic), and established the interaction between the virtual keyboard and the guess grid.
* **Sprint 2 (Features & UI Enhancement):** Introduced the retro pixel-art aesthetics, integrated the Web Audio API for sound feedback (keystrokes, win/lose SFX), and developed the dual-difficulty system (4x4 Easy and 6x6 Hard modes).
* **Sprint 3 (Advanced Systems & Testing):** Implemented the `localStorage`-driven level unlocking progression system, developed the dynamic dictionary filtering algorithm for the right-side hint panel, and finalized the Developer Mode for final testing and Demo recording.

### Members (Roles & Responsibilities & Portion)
*The total contribution portion for all members is 100%.*

* **LIN HONGHUA [33.34%]**:
    * **Responsibilities:** Project Lead; designed the core scoring algorithm; implemented the UI/UX interface and retro pixel-art aesthetics; integrated the Web Audio sound system and designed the Developer Mode architecture.
* **CHENG KWING LEUNG [33.33%]**:
    * **Responsibilities:** Dictionary integration and data cleaning for word lists; implemented the dynamic dictionary filtering algorithm; conducted cross-browser compatibility testing and level progression logic testing.
* **DENG SIYI [33.33%]**:
    * **Responsibilities:** Authored the project documentation (README.md) and Appendix A (Contribution Form); documented the Generative AI usage and declaration (Appendix B); performed quality assurance and frontend interaction logic testing for the "Game Rules" and "Game Over" panels.

### Schedule
* **Week 1:** Requirement analysis, UI sketch design, and basic architecture setup.
* **Week 2:** Completed the core gameplay logic for the 4x4 mode and data binding between the virtual keyboard and the guess grid.
* **Week 3:** Expanded the dictionary for the 6x6 mode, and developed advanced features (hint panel, audio system, local progress saving mechanism).
* **Week 4:** Comprehensive debugging, code optimization, Demo Video recording, and completion of the README and related final project documentation.

### Algorithm
The core algorithms of this software consist of two main parts:
1. **Scoring Algorithm:**
    * When a user submits a guess, the system first verifies its length and checks it against the dictionary.
    * **Exact Match (Green):** Iterates to compare the guess with the target word; if `guess[i] === target[i]`, it is marked as `correct`.
    * **Position Match (Yellow):** Calculates the frequency of remaining letters in the target word. If `guess[i]` exists in the remaining letters, it is marked as `wrong-location`, and the frequency count of that letter is decremented to accurately handle "duplicate letters".
    * **Miss (Grey):** All other letters are marked as `absent`.
2. **Dynamic Hint Generation Algorithm:**
    * The system maintains a `correctLetters` dictionary in the background, tracking all discovered green letters and their absolute index positions.
    * After each valid submission, the system iterates through the complete dictionary of the current difficulty, using a higher-order function (`Array.prototype.filter`) to extract all candidate words that "perfectly match the known letters" at the specific indices, and dynamically renders them on the right-side UI panel.

### Current status of your software
**Completed and running stably at the demonstration stage.** The software currently features full playability, supporting Visitor Mode (including level selection, unlocking, and local progress saving) and Developer Mode (including privileged login and direct answer display). It has also perfectly integrated smooth CSS flip/shake animations and interactive sound effects.

### Future plan
* **Backend Integration:** Introduce a Node.js backend server and database to support real user registration, login, and cloud progress saving.
* **Leaderboard System:** Implement a Global Leaderboard based on clearance time or minimum attempt counts.
* **Other Game Modes:** Consider adding a Daily Challenge or Endless Mode to increase the game's replayability and user retention.

---

## Environments of the software development and running

* **Programming Language:** HTML5, CSS3, JavaScript (ES6+ / Vanilla JS).
* **Minimum H/W requirements:** Any terminal device with a display and input method (keyboard, mouse, or touch screen). At least 1GB RAM is recommended to ensure smooth DOM manipulation and audio buffering.
* **Minimum S/W requirements:** Modern web browsers supporting HTML5 and ES6 syntax (e.g., Google Chrome, Mozilla Firefox, Apple Safari, Microsoft Edge).
* **Required packages:** None. This project relies entirely on native Web APIs (including `AudioContext` for sound effects) and **does not use** any third-party JavaScript frameworks or dependency packages (such as React, Vue, jQuery, etc.).

---

## Declaration

* The core code logic, UI layout, and interactive features of this project (Arcane Lexicon) were independently hand-coded by our team members.
* The spelling validation logic in the game is inspired by the classic Wordle game rules.
* The built-in English dictionaries were consolidated from open-source datasets on the internet and underwent manual filtering and data cleaning by our team.
* No undeclared open-source packages from non-team members were used.
* **Generative AI Statement:** Generative AI was used to assist in brainstorming UI aesthetic inspirations and refining the sentence structures of some technical documentation.

---

## Demo (Youtube URL)

**https://youtu.be/ETLTK0QqI_Q**
