# AI Problem Solving Assessment

> **Register Number**: RA2411026050043

> 🌐 **Live Website**: [https://chethanbugide-png.github.io/AI_ProblemSolving_RA2411026050043/](https://chethanbugide-png.github.io/AI_ProblemSolving_RA2411026050043/)

Interactive AI-powered web applications: a Wumpus World exploration game with AI inference, and a real-time Emergency Command Center with 5 AI modules.

---

## 📁 Repository Structure

```
AI_ProblemSolving/
├── Problem15_WumpusWorld/
│   └── wumpus_world.html          # Wumpus World Game + AI Inference
├── Problem20_EmergencyResponse/
│   └── emergency_response.html    # Emergency Command Center
└── README.md
```

---

## Problem 15: Wumpus World Decision System (AI Inference Game)

### 📋 Problem Description
A robot navigates an unknown cave with hidden pits and a Wumpus. Using percepts (breeze, stench, glitter), the AI inference engine deduces safe/risky/deadly cells.

### 🧠 Algorithms Used
| Algorithm | Purpose |
|-----------|---------|
| **Rule-Based Inference** | Deduce cell safety from percept patterns at visited cells |
| **BFS Pathfinding** | Find shortest safe path to unexplored cells |
| **Knowledge Base** | Accumulate risk scores from breeze/stench convergence |

### ▶️ How to Play
1. Open `wumpus_world.html` in any browser
2. Choose grid size & difficulty → **Enter the Cave**
3. **Move**: Arrow keys / WASD / click adjacent cells
4. **Shoot**: `F` key → choose direction to kill Wumpus
5. **Grab Gold**: `G` key on gold cell
6. **Escape**: `C` key at (1,1) to win

### 📊 Game Mechanics
| Percept | Meaning |
|---------|---------|
| 💨 Breeze | Adjacent pit |
| 🦨 Stench | Adjacent Wumpus |
| ✨ Glitter | Gold on cell |
| Win | Grab gold + escape = +2000 pts |
| Lose | Pit or Wumpus = –1000 pts |

---

## Problem 20: Smart Emergency Response — Command Center

### 📋 Problem Description
A real-time emergency command center that handles concurrent crises using 5 integrated AI modules for decision-making, dispatch, and route planning.

### 🧠 Algorithms Used
| Algorithm | Purpose |
|-----------|---------|
| **A\* Graph Search** | Find optimal rescue & hospital routes through city graph |
| **CSP** | Assign ambulances, hospitals, teams by availability & speciality |
| **Rule-Based System** | Classify priority (HIGH/MEDIUM/LOW) via 5 weighted rules |
| **Means-Ends Analysis** | Generate 8-step rescue plan from detection to closure |
| **ML Classification** | Predict severity from 5 normalized features |

### ▶️ Execution Steps
1. Open `emergency_response.html` in any browser
2. Use presets or fill the form; click map nodes to select location
3. Click **🚨 DISPATCH EMERGENCY**
4. Watch animated vehicles travel routes on the city map
5. Dispatch multiple emergencies — resources update in real-time
6. Emergencies auto-resolve after ~15–25 seconds

### 📊 Key Features
- **Live Command Bar**: Clock, alert level (NORMAL/ACTIVE/CRITICAL), active & resolved counts
- **Animated City Map**: Vehicle dots travel along A* routes in real-time, emergency pulse rings
- **Concurrent Emergencies**: Dispatch multiple — resources marked busy until resolved
- **Three-Panel Layout**: Input+Resources | City Map | AI Analysis + Timeline

---

## 🛠 Technologies
- **HTML5 / CSS3 / JavaScript** — Single-file, zero dependencies
- **Canvas API** — DPI-aware animated city map
- **requestAnimationFrame** — Smooth 60fps dispatch animations
- No server needed — just open in any modern browser
