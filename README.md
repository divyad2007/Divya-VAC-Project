# DSA Visual Guide: Interactive Computer Science Learning Platform & Capstone Workstation

> **Capstone 11 Project**  
> **Student / Author:** DHINESH  
> **Department:** Computer Science & Engineering  
> **Tech Stack:** React 19, Tailwind CSS v4, Vite 8, Web Audio API, Recharts, Canvas Confetti, Google Gemini Generative AI

---

## 🌟 Overview

**DSA Visual Guide** is an interactive, zero-external-server learning platform designed to bridge the spatial mental model gap in Data Structures & Algorithms (DSA). Traditional textbook instruction often fails to communicate dynamic pointer mutations, recursive divide-and-conquer partitions, self-balancing tree rotations, and state transitions. 

This platform transforms abstract data structures into tactile, observable visual states with synchronized auditory feedback, client-side code execution in C, C++, and Python, real-time asymptotic complexity curves, and AI pedagogical tutoring.

---

## 🚀 Key Modules & Capabilities

### 1. 📊 Interactive Visualizer Hub (`/visualizer`)
- **Arrays & 5 Sorting Algorithms:** Bubble Sort, Selection Sort, Insertion Sort, Merge Sort, and Lomuto QuickSort with real-time partition boundaries, plus Linear Search and Binary Search with bounds visualization.
- **Linked Lists:** Singly, Doubly, and Circular linked lists with interactive head/tail insertion, node deletion, pointer redirection animations, and memory cleanup highlighting.
- **Stacks:** Dual-mode (Array-based fixed capacity vs Pointer-based dynamic heap list) with LIFO enforcement, peek idempotence, and visual overflow / underflow alerts.
- **Queues & Deque:** 4 variants including Linear Queue, Circular Modulo Wrapping Queue (`(rear + 1) % CAPACITY`), Priority Queue (min-heap order), and Double-Ended Queue (Deque).
- **Self-Balancing Trees:** Binary Search Tree (BST) traversals (In-order, Pre-order, Post-order) and AVL Trees featuring real-time node Balance Factor calculations ($\text{BF} \in \{-1, 0, +1\}$) with animations for LL, RR, LR, and RL rotations.
- **Graphs:** Interactive 2D graph canvas with vertex dragging, directed/undirected edges, and real-time execution of BFS, DFS, and Dijkstra's Shortest Path Algorithm with distance table updates.

### 2. 📈 Big-O Asymptotic Complexity Engine (`/complexity`)
- Dynamic interactive SVG growth curves ($O(1)$, $O(\log n)$, $O(n)$, $O(n \log n)$, $O(n^2)$, $O(2^n)$) powered by Recharts.
- Real-time input size slider ($n = 1$ to $500$).
- Hardware CPU clock cycle translator calculating wall-clock execution latency estimates on 3.0 GHz processors.
- Master Theorem and recurrence relation references.

### 3. 💻 Code Practice & Execution Sandbox (`/practice`)
- 30+ curated DSA coding challenges graded across Easy, Medium, and Hard.
- In-browser safe client-side JavaScript execution sandbox.
- 3-tier progressive hints per problem.
- Multi-language reference solutions in **Python**, **C++**, and **C**.

### 4. 🧪 10-Test Integration Suite (`/testing`)
Automated verification harness running deterministic unit tests:
1. Bubble Sort Stability & Numerical Correctness
2. QuickSort Partitioning & Edge Cases (Duplicates & Sorted input)
3. Binary Search Midpoint Overflow Safety ($low + (high - low) / 2$)
4. Singly Linked List Head/Tail Pointer Operations
5. Doubly Linked List Bi-directional Linkage (`node.next.prev === node`)
6. Stack LIFO Invariant & Capacity Overflow Guard
7. Circular Queue Modulo Wrap-around
8. BST In-Order Traversal Monotonicity
9. AVL Self-Balancing Tree Invariant ($|\text{BF}| \le 1$)
10. Dijkstra Shortest Path Optimality on Weighted Graph

### 5. 🤖 Gemini AI Study Companion (`/ai`)
- Integrates Google Gemini API with secure local storage of user API keys.
- **100% Offline Knowledge Base:** Intelligent rule-based fallback providing detailed explanations, analogies, code reviews, and practice questions even without an API key or internet access.
- Pre-configured prompt shortcuts for quick queries.

### 6. 🔄 Before & After Pedagogical Comparisons (`/before-after`)
- **Visual vs Textbook Learning:** Side-by-side breakdowns of QuickSort partitioning, AVL rotations, and Dijkstra path relaxation.
- **Code Bug Corrections:** Common student pitfalls including 32-bit integer overflow in binary search, linked list memory leaks, and circular queue false overflow.
- **Asymptotic Optimizations:** Quadratic to Linear reductions ($O(n^2) \to O(n)$ Two Sum, $O(2^n) \to O(n)$ Fibonacci, $O(n^3) \to O(n)$ Kadane).

### 7. 📑 Prompt Engineering Blueprint Library (`/prompts`)
- 7 battle-tested engineering prompt blueprints for ChatGPT, Gemini, and Claude.
- 1-click copy to clipboard with toast notification.
- "Send to AI Assistant" direct pipeline.

### 8. 🎓 7-Slide Capstone Project Defense Deck (`/presentation`)
- Slide 1: Introduction & Problem Statement
- Slide 2: Architecture & Design Pipeline
- Slide 3: Interactive Data Structure Modules
- Slide 4: Big-O Asymptotic Complexity Engine
- Slide 5: Code Practice & Automated Test Harness
- Slide 6: Bilingual Pedagogy & Gemini AI Tutor
- Slide 7: Results, Impact & Future Roadmap
- Features presenter speech notes, keyboard navigation (Space / Arrow keys), full-screen mode, and live visualizer jump links.

### 9. 📝 Bilingual Concept Notes & Cheat Sheets (`/notes` & `/cheatsheets`)
- Bilingual study guides with formal English and regional Tamil/Tanglish summaries.
- Printable, high-yield one-page revision cheat cards.

### 10. 🏆 15-Question Assessment Quiz (`/quiz`)
- University exam level multiple choice assessment with score history and canvas celebration confetti.

---

## 🛠️ Running Locally

```bash
# Clone the repository
git clone <repo-url>
cd DHINESH

# Install dependencies
npm install

# Start development server
node ./node_modules/vite/bin/vite.js
# Or standard:
npm run dev

# Build for production
node ./node_modules/vite/bin/vite.js build
```

---

## 📦 Project Structure

```
DHINESH/
├── src/
│   ├── components/
│   │   ├── ai/            # AI Study Assistant (Gemini + Offline fallback)
│   │   ├── compare/       # Before & After pedagogical comparisons
│   │   ├── complexity/    # Big-O chart and growth rate curves
│   │   ├── dashboard/     # Learning streak, stats, and quick launchpad
│   │   ├── demo/          # Automated guided tour walkthrough
│   │   ├── layout/        # Navbar and responsive Sidebar
│   │   ├── notes/         # Concept Notes (Bilingual) & Cheat Sheets
│   │   ├── practice/      # 30+ runnable coding problems & solutions
│   │   ├── presentation/  # 7-Slide Project Defense deck with speaker notes
│   │   ├── prompts/       # Prompt Engineering Blueprint Library
│   │   ├── quiz/          # 15-Question DSA assessment with confetti
│   │   └── visualizers/   # Arrays, LinkedLists, Stacks, Queues, Trees, Graphs
│   ├── context/
│   │   └── DSAContext.jsx # Global state, sound, theme, bookmarks & streaks
│   ├── data/              # Curated datasets, questions, problems, and prompts
│   ├── utils/
│   │   ├── dsaAlgorithms.js # Pure step generators for all algorithms
│   │   └── soundEffects.js  # Web Audio API acoustic synthesizer
│   ├── App.jsx            # Master layout & dynamic view routing
│   ├── index.css          # Glassmorphism tokens & dark/light theme
│   └── main.jsx
├── package.json
└── vite.config.js
```

---

## 👨‍💻 Author
**DHINESH**  
Department of Computer Science & Engineering  
*Capstone 11: Interactive Data Structures & Algorithms Workstation*
