# Quiz Game (Unity)

## Project Description

This project is a **Quiz Game developed in Unity** as part of the course **Introduction to Game Development**.

The game consists of **three different quiz levels**, each with a different type of question interaction:

* Multiple choice questions
* True / False questions
* Word input questions

The player progresses through levels while answering questions and receives a final score at the end of the game.


---

# Game Structure

## Scenes

The game contains **5 scenes**:

1. **MainMenu**
2. **QuizLevel1**
3. **QuizLevel2**
4. **QuizLevel3**
5. **GameOver**

### MainMenu

Main screen of the game where the player can start or exit.

UI Elements:

* Start Button
* Quit Button

---

### QuizLevel1

The first quiz level with **multiple choice questions**.

UI Elements:

* Question Panel
* 4 buttons with answer options

---

### QuizLevel2

The second level with **True / False questions**.

UI Elements:

* Question Panel
* True Button
* False Button

---

### QuizLevel3

The final level where the player must **type the correct word**.

UI Elements:

* Question Panel
* Input Field
* Submit Button

---

### GameOver

Final screen showing the player's result.

UI Elements:

* Result Text displaying the final score

---

# Scripts

All scripts are stored in the **Scripts** folder.

## GameManager

Responsible for the main game logic:

* storing questions
* tracking player score
* handling level transitions
* restarting the game
* saving the final result

---

## Question

Defines the **Question class**, which represents a quiz question used in the game.

---

## UIManager

Handles:

* displaying questions
* processing user answers
* updating score
* moving to the next level

---

## WordGameManager

Controls the gameplay of the **word input level**:

* displaying scrambled words
* checking player input
* updating score
* progressing through the level

---

## MainMenu

Controls the functionality of the **Main Menu**.

Functions include:

* starting the game
* exiting the application

---

## ResultManager

Manages the **GameOver screen**:

* displays player score
* handles restart or exit options

---

# Scene Managers

Each scene has an **Empty GameObject** that acts as a manager.

Scripts attached to scene objects:

| Scene      | Manager Object  | Script          |
| ---------- | --------------- | --------------- |
| MainMenu   | MainMenuManager | MainMenu        |
| MainMenu   | GameManager     | GameManager     |
| QuizLevel1 | QuizManager     | UIManager       |
| QuizLevel2 | QuizManagerTF   | UIManager       |
| QuizLevel3 | WordGameManager | WordGameManager |
| GameOver   | ResultManager   | ResultManager   |

Buttons are connected using:

```
OnClick → SceneManager → Choose Function
```

---

# Event System

Each scene contains an **EventSystem** object to support UI interaction.

---

# Questions Configuration

All questions are configured in:

```
MainMenu Scene → GameManager
```

This object stores the quiz questions used throughout the game.

---

# Build Settings

Before running the game, make sure all scenes are added to the build settings:

```
File → Build Settings → Add Open Scenes
```

Scenes included:

* MainMenu
* QuizLevel1
* QuizLevel2
* QuizLevel3
* GameOver

---

# How to Run

1. Open the project in **Unity**.
2. Open the **MainMenu scene**.
3. Press **Play** in the Unity Editor.


![alt text](https://github.com/verochka458/Simple-Quiz-in-Unity/blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202025-04-27%20223124.png)

![alt text](https://github.com/verochka458/Simple-Quiz-in-Unity/blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202025-04-27%20223900.png)

![](https://github.com/verochka458/Simple-Quiz-in-Unity/blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202025-04-27%20223148.png)

![](https://github.com/verochka458/Simple-Quiz-in-Unity/blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202025-04-27%20223835.png)

![](https://github.com/verochka458/Simple-Quiz-in-Unity/blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202025-04-27%20223336.png)
