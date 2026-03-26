# 🔤 Unscramble

A single-player Android word game where players unscramble shuffled words. Built with Kotlin and modern Android Architecture Components.

---

## 📖 About

Unscramble presents the player with a scrambled word and challenges them to rearrange all the letters to form the correct word. The app demonstrates clean Android development practices using **ViewModel** and **StateFlow** for reactive UI state management.

---

## 🎮 How to Play

1. A scrambled word is displayed on the screen.
2. Type your guess using all the letters shown.
3. Tap **Submit** to check your answer.
4. If correct, your score increases and the next word appears.
5. Tap **Skip** to move to the next word without scoring.
6. The game ends after 10 words — try to get the highest score!

---

## ✨ Features

- Randomized scrambled words each game session
- Score tracking across rounds
- Skip option for difficult words
- Input validation with error feedback
- Clean game-over summary screen
- Fully reactive UI with no data loss on screen rotation

---

## 🏗️ Architecture

This project follows the **MVVM (Model-View-ViewModel)** pattern recommended by Google:

```
UI Layer  ──▶  ViewModel  ──▶  Data / Game Logic
   ▲                │
   └── StateFlow ───┘
```

| Component | Role |
|-----------|------|
| `GameViewModel` | Holds and manages all UI-related game state |
| `StateFlow` | Exposes state as a reactive stream to the UI |
| `Fragment / Activity` | Observes state and renders the UI |

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **Kotlin** | Primary language (100%) |
| **Android ViewModel** | Survive configuration changes |
| **StateFlow / Coroutines** | Reactive state management |
| **View Binding** | Type-safe view access |
| **Gradle (Kotlin DSL)** | Build configuration via `.kts` files |
| **Material Design** | UI components and styling |

---

## 🚀 Getting Started

### Prerequisites

- Android Studio **Flamingo** or later
- JDK 11+
- Android SDK with minimum API level **26**

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/RishiJadhav01/Unscramble.git
   ```

2. **Open in Android Studio**
   - Launch Android Studio
   - Select **File → Open** and navigate to the cloned folder

3. **Build and run**
   - Wait for Gradle sync to complete
   - Select a device or emulator
   - Click **Run ▶**

---

## 📁 Project Structure

```
Unscramble/
├── app/
│   └── src/
│       └── main/
│           ├── java/         # Kotlin source files
│           │   └── ...       # ViewModel, UI, data
│           └── res/          # Layouts, strings, drawables
├── gradle/
├── build.gradle.kts
├── settings.gradle.kts
└── README.md
```
