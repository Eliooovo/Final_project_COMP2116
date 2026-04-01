# A Daily Word Game (Simplified Version)
## 1. Graphical Abstract
<img width="600" height="600" alt="game_preview" src="https://github.com/user-attachments/assets/53a599ac-e31e-4ce9-9ac4-9e534f9bac43" />

> *Quick look at the gameplay: Four letters, four tries, one goal.**Quick look at the gameplay: Four letters, four tries, one goal.*

---

## 2. Purpose of the Software
* **Software Development Process**: We adopted the **Agile Development Model**.
    * **Reasoning**: Agile allows for iterative updates. Since game mechanics (like animations and state management) require frequent testing and refinement, an iterative approach ensured that the core loop was functional before adding visual polish.
* **Target Market**: Casual gamers, English learners, and puzzle enthusiasts looking for a quick mental exercise.

## 3. Software Development Plan
### Development Stages:
1.  **Requirement Analysis**: Defined the 4x4 constraint (4 letters, 4 attempts).
2.  **UI/UX Design**: Built a responsive grid and virtual keyboard using CSS Grid/Flexbox.
3.  **Logic Implementation**: Developed the comparison algorithm to handle character states.
4.  **Testing & Refinement**: Implemented "Shake" and "Dance" animations for feedback.

### Team Roles & Contributions:
* **Member A (40%)**: Lead UI/UX Designer & CSS Animator.
* **Member B (30%)**: Logic Developer (JavaScript state management).
* **Member C (30%)**: Documenter & Video Editor.

### Algorithm Description:
The game uses a **Character-State Logic**:
* `correct`: Letter exists and is in the right position (Green).
* `present`: Letter exists but is in the wrong position (Yellow).
* `absent`: Letter is not in the word (Gray).

### Current Status & Future Work:
Currently at **Pilot Level**. Future plans include adding global leaderboards and a "Hard Mode" with longer words.

## 4. Environments
* **Languages**: HTML5, CSS3, JavaScript (Vanilla).
* **Hardware**: Any device with a modern web browser.
* **Software**: Tested on Google Chrome, Safari, and Firefox.
* **Dependencies**: None (Zero-dependency project).

## 5. Declaration
The CSS layout and animation logic (Shake/Dance) were inspired by open-source Wordle clones and optimized for this 4-letter version.
