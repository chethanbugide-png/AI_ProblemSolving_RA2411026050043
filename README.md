<div align="center">

# 🧠 AI Problem Solving

### *Interactive AI-Powered Web Applications*

[![GitHub Pages](https://img.shields.io/badge/🌐_Live_Demo-Visit_Website-2ea44f?style=for-the-badge)](https://chethanbugide-png.github.io/AI_ProblemSolving_RA2411026050043/)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github)](https://github.com/chethanbugide-png/AI_ProblemSolving_RA2411026050043)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Canvas API](https://img.shields.io/badge/Canvas_API-FF6384?style=flat-square&logo=html5&logoColor=white)

**Register Number** · `RA2411026050043`




</div>

---

## 📁 Project Structure

```
AI_ProblemSolving_RA2411026050043/
│
├── 🎮 WumpusWorld/
│   └── wumpus_world.html              ← AI Inference Game
│
├── 🚨 EmergencyResponse/
│   └── emergency_response.html        ← Command Center Dashboard
│
├── 🏠 index.html                       ← Landing Page (GitHub Pages)
├── 📄 README.md
└── ⚙️ .github/workflows/static.yml    ← Auto-deploy to GitHub Pages
```

---

<div align="center">

## ⚔️ Wumpus World

### *AI Inference Game with Fog-of-War Exploration*

</div>

### 🎯 Problem Statement

> A robot is deployed in a hazardous mining environment where it must navigate safely while avoiding dangers such as **pits** and a hidden **Wumpus**. The robot receives environmental signals (percepts) like **breeze** and **stench** to infer the safety of nearby cells.

### 🧠 Algorithms Implemented

| # | Algorithm | What It Does |
|---|-----------|-------------|
| 1 | **Rule-Based Inference** | Analyzes percepts (breeze → pit nearby, stench → wumpus nearby) to classify each unexplored cell as `SAFE`, `RISKY`, or `DEADLY` |
| 2 | **BFS Pathfinding** | Finds the shortest safe path from the player's position to unexplored safe cells |
| 3 | **Knowledge Base Engine** | Accumulates risk scores when multiple percept sources converge on the same cell, increasing confidence in danger classification |

### 🎮 How to Play

| Action | Keyboard | Mouse |
|--------|----------|-------|
| **Move** | `Arrow Keys` / `W A S D` | Click adjacent cell |
| **Shoot Arrow** | `F` then direction key | — |
| **Grab Gold** | `G` | — |
| **Climb Out** | `C` (at start cell) | — |

### 🌟 Game Features

- 🌫️ **Fog of War** — Cave is hidden; cells reveal as you explore
- 🤖 **AI Advisor Panel** — Real-time inference showing safe/risky/deadly cells
- 🛤️ **Suggested Paths** — BFS-computed routes to nearest safe unexplored cells
- 🏹 **Arrow Shooting** — Fire arrows to kill the Wumpus from a distance
- 💎 **Gold Collection** — Find gold and escape for maximum score
- ⚙️ **Configurable** — Grid size (4-6), difficulty (2-4 pits), wumpus count (1-2)
- 🏆 **Score System** — `+1000` gold, `+1000` escape, `-1` per move, `-1000` death

### 📊 Percept Reference Table

| Percept | Symbol | Meaning | AI Inference |
|---------|--------|---------|-------------|
| Breeze | 💨 | Adjacent cell has a **Pit** | Neighboring cells get `pit_risk++` |
| Stench | 🦨 | Adjacent cell has the **Wumpus** | Neighboring cells get `wumpus_risk++` |
| Glitter | ✨ | **Gold** is on this cell | Mark as high-value target |
| Nothing | ✅ | Cell is completely safe | All neighbors confirmed safe from this direction |

### 📋 Sample Input & Output

<table>
<tr><td>

**Input (3×3 Grid)**
```
(1,1) → Safe
(1,2) → Breeze
(1,3) → Stench
(2,1) → Breeze
(2,2) → Safe
(2,3) → Unknown
```

</td><td>

**AI Inference Output**
```
✅ Safe Cells    → (1,1), (2,2)
⚠️ Risky Cells   → (2,3) wumpus risk
☠️ Deadly Cells  → None confirmed
🛤️ Safe Path     → (1,1) → (2,2)
```

</td></tr>
</table>

> **Reasoning**: Breeze at (1,2) and (2,1) → pit risk at their neighbors. Stench at (1,3) → wumpus risk at (2,3). Cell (2,2) has no percepts → confirmed safe.

---

<div align="center">

## 🚨 Emergency Command Center

### *Real-Time Multi-Module AI Decision Support System*

</div>

### 🎯 Problem Statement

> A smart city emergency system is designed to respond to different crisis situations such as accidents, disasters, and medical emergencies. The system must assist in **decision-making**, **resource allocation**, and **route planning** in real time using multiple AI techniques.

### 🧠 Five AI Modules

| # | Module | Technique | Output |
|---|--------|-----------|--------|
| 1 | **Route Finder** | `A* Graph Search` | Optimal rescue route (station → scene) and hospital transport route (scene → hospital), with distances and ETA |
| 2 | **Resource Allocator** | `Constraint Satisfaction (CSP)` | Assigns best ambulance, hospital, and rescue team based on availability, speciality match, and proximity |
| 3 | **Priority Classifier** | `Rule-Based System` | Classifies emergency as `HIGH` / `MEDIUM` / `LOW` using 5 weighted rules (injury, victims, risk, type, delay) |
| 4 | **Action Planner** | `Means-Ends Analysis` | Generates 8-step rescue plan from emergency detection through incident closure |
| 5 | **Severity Predictor** | `ML Classification` | Predicts severity from 5 normalized features using a weighted decision model with confidence score |

### 🌟 Key Features

- 📡 **Live Command Bar** — Real-time clock, alert level (`NORMAL` → `ACTIVE` → `CRITICAL`), active/resolved counts
- 🗺️ **Interactive City Map** — Canvas-rendered 8-node city graph with animated vehicle dispatch at 60fps
- 🚑 **Animated Dispatch** — Vehicle dots physically travel along A* routes in real-time
- 📍 **Click-to-Select** — Click any node on the map to set emergency location
- ⚡ **Concurrent Emergencies** — Dispatch multiple crises simultaneously; resources go busy and auto-restore
- 🟢🟠🔴 **Resource Tracking** — Live status indicators (available / dispatched / unavailable)
- 📜 **Event Timeline** — Chronological log of every dispatch action
- 🎯 **Preset Scenarios** — Quick-fill buttons for Accident, Fire, Medical, Flood, Chemical

### 🏙️ City Graph

```
    [A] Downtown HQ ──── 4km ──── [B] Central Station ──── 6km ──── [C] Highway
     │                              │                                  │
    5km                            3km                                4km
     │                              │                                  │
    [D] Suburb Hospital ─ 4km ── [E] Residential ──── 5km ──── [F] Industrial
     │                           │    │                                │
    3km                        5km  6km                              3km
     │                         │      │                                │
    [G] Medical Center ── 7km ──────── [H] East Outpost ──────────────┘
```

> 🟣 HQ (Hospital + Station) · 🔵 Station · 🟢 Hospital · ⚪ Zone

### 📋 Sample Input & Output

<table>
<tr><td width="50%">

**Input**
```
Type:     🔥 Building Fire
Location: Industrial Area (F)
Injury:   Critical
Victims:  5
Risk:     High
Delay:    3 min
```

</td><td width="50%">

**Output**
```
⚡ Priority:   HIGH (Score: 85/100)
🤖 ML Severity: High (conf: 92%)
🛤️ Route:      F → scene → G (hospital)
🚑 Ambulance:  AMB-03 (Advanced, Node F)
🏥 Hospital:   City Medical Ctr (Burns & ICU)
🧑‍🚒 Team:      Charlie Unit (HazMat)
📐 Plan:       8-step action plan generated
```

</td></tr>
</table>

### 📐 Rule-Based Priority Scoring

| Rule | Condition | Points |
|------|-----------|--------|
| **Injury** | Critical: 40 · Severe: 25 · Moderate: 12 · Minor: 5 | `0-40` |
| **Victims** | ≥10: 30 · ≥5: 20 · ≥2: 10 · 1: 3 | `3-30` |
| **Zone Risk** | High: 15 · Medium: 8 · Low: 2 | `2-15` |
| **Type** | Fire/Chemical/Collapse: 15 · Flood: 10 · Other: 5 | `5-15` |
| **Delay** | ≥30min: 15 · ≥15min: 8 · <15min: 2 | `2-15` |
| | **Total** | `/100` |
| | HIGH ≥ 60 · MEDIUM ≥ 35 · LOW < 35 | |

---

<div align="center">

## 🚀 Quick Start

</div>

```bash
# Clone the repository
git clone https://github.com/chethanbugide-png/AI_ProblemSolving_RA2411026050043.git

# Open any HTML file directly in your browser
# No server, no build, no dependencies needed!

# Option 1: Wumpus World Game
start WumpusWorld/wumpus_world.html

# Option 2: Emergency Command Center
start EmergencyResponse/emergency_response.html

# Option 3: Landing Page
start index.html
```

Or visit the **[🌐 Live Demo](https://chethanbugide-png.github.io/AI_ProblemSolving_RA2411026050043/)** — no installation required.

---

<div align="center">

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Structure** | HTML5 Semantic Elements |
| **Styling** | CSS3 (Custom Properties, Gradients, Animations, Grid, Flexbox) |
| **Logic** | Vanilla JavaScript (ES6+) |
| **Graphics** | Canvas API (DPI-aware, 60fps animation loop) |
| **Fonts** | Inter, JetBrains Mono (Google Fonts) |
| **Deploy** | GitHub Pages + GitHub Actions |
| **Backend** | ❌ None — fully client-side |
| **Dependencies** | ❌ Zero — no frameworks, no libraries |

---

**Made with 💻 by Chethan** · RA2411026050043

</div>
