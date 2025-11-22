# 🎰 Universal Lottery Simulation System

![React](https://img.shields.io/badge/React-18.2.0-blue)
![Vite](https://img.shields.io/badge/Vite-4.4.5-purple)
![License](https://img.shields.io/badge/License-MIT-green)

A full‑featured web platform for designing, simulating, and analyzing any lottery systems using a powerful visual builder and simulation engine.

---

## 📋 Table of Contents
- [🎯 Features](#-features)
- [🚀 Quick Start](#-quick-start)
- [🏗️ Architecture](#️-architecture)
- [🎫 Ticket Field Types](#-ticket-field-types)
- [🎲 Draw Mechanisms](#-draw-mechanisms)
- [🏆 Winning Conditions](#-winning-conditions)
- [📊 Sales Variability](#-sales-variability)
- [🔧 Implementation Details](#-implementation-details)
- [📈 Example Configurations](#-example-configurations)
- [🎯 Usage](#-usage)

---

# 🎯 Features

## 🧩 Visual Builder
- Drag‑and‑drop rule creation  
- Step ordering and dependencies  
- Real‑time preview  
- Import/Export JSON configurations  

## ⚡ Advanced Simulation
- Monte‑Carlo multi‑run simulation  
- Sales variability modeling  
- Detailed metrics and comparison dashboards  

## 📈 Deep Analytics
- Financial performance charts  
- Prize distribution analysis  
- Draw-by-draw historical breakdown  

## 🎯 Flexibility
- Works with ANY lottery type  
- Highly customizable mechanics  
- JavaScript-based winning rules  
- Multi‑stage drawing workflows  

---

# 🚀 Quick Start

### Requirements
- Node.js **16+**
- npm **7+**

### Installation
```bash
git clone <repository-url>
cd lottery-simulator

npm install
npm run dev
npm run build
```

App runs at: **http://localhost:3000**

---

# 🏗️ Architecture

```
src/
├── components/
│   ├── RuleBuilder.js
│   ├── LotteryPreview.js
│   ├── Simulation.js
│   └── AnalysisDashboard.js
├── App.js
└── App.css
```

### Core Engine: `UniversalLotteryEngine`
Handles:
- Ticket generation  
- Draw execution  
- Condition evaluation  
- State management  
- Statistics aggregation  

```javascript
const engine = new UniversalLotteryEngine(config);
const result = engine.simulateSingleDraw(1000);
```

---

# 🎫 Ticket Field Types

### Number
```javascript
{ type: 'number', min: 1, max: 50 }
```

### Choice
```javascript
{ type: 'choice', options: ['red','blue','green'] }
```

### Boolean
```javascript
{ type: 'boolean' }
```

### Special
```javascript
{ type: 'special', specialType: 'luckyNumber' }
```

### Sequential Unique
```javascript
{ type: 'sequentialUnique', poolId: 'serial_numbers' }
```

---

# 🎲 Draw Mechanisms

Examples:

```javascript
{ mechanism: 'randomRange', min: 1, max: 50 }
{ mechanism: 'weightedChoice', options: [...], weights: [...] }
{ mechanism: 'multipleNumbers', count: 6 }
{ mechanism: 'sequence', sequence: ['winter','spring','summer','fall'] }
{ mechanism: 'sequentialUniqueChoice', poolId: 'grand_prizes' }
```

---

# 🏆 Winning Conditions

Conditions are JavaScript expressions:

```javascript
"ticket.number === draw.winner"
```

Prize types:
- `fixed`
- `jackpot`
- `percentage`

---

# 📊 Sales Variability
```javascript
{ type: 'percentage', value: 15 }
```

Supported:
- none  
- percentage  
- fixed  
- minMax  

---

# 🔧 Implementation Details

### System State Example
```javascript
{
  currentJackpot: 1000000,
  totalSales: 0,
  totalPayouts: 0,
  jackpotsWon: 0,
  drawHistory: []
}
```

### Safe Condition Evaluation
```javascript
new Function('ticket', 'draw', `return ${condition}`)
```

---

# 📈 Example Configurations

Includes:
- 6/45 Classic Lottery  
- Promo‑code Lottery  
- Multi‑stage Space Lottery  

(Full configs omitted for brevity — available in the full documentation.)

---

# 🎯 Usage

Standard flow:
1. Design lottery structure  
2. Configure via visual builder  
3. Test & simulate  
4. Analyze results  
5. Optimize & rerun  

---

If you need:
✔ full documentation  
✔ a richer GitHub page (badges, screenshots, GIF demos)  
✔ multiple language versions  

— I can generate those too!
