#  Character-Level Name Generator

A lightweight AI-inspired project that generates realistic names using a **character-level probabilistic model (Markov Chain)**.

---

## 🚀 Overview

This project builds a **weighted directed graph** from a dataset of names, where:

* Each node represents a **character**
* Each edge represents a **transition between characters**
* Edge weights represent how frequently transitions occur

Using this graph, the system generates new names by sampling probable character sequences.

---

## ✨ Features

* 🔤 Character-level name generation
* 📊 Weighted transition graph (Markov model)
* 🎲 Probabilistic name sampling
* 🎨 Graph visualization with:

  * Weighted edges (thicker = more frequent)
  * Color gradients (purple → violet)
  * Alpha blending (opacity based on importance)
  * Special nodes:

    * `^` (start) → green
    * `$` (end) → red

---

## 🧠 How It Works

1. **Preprocessing**

   * Cleans dataset (removes non-English names, null values)
   * Normalizes text (lowercase, trims spaces)

2. **Graph Construction**

   * Adds special tokens:

     * `^` → start of name
     * `$` → end of name
   * Builds transitions:

     ```
     ^ → s → a → n → d → y → $
     ```
   * Updates edge weights for repeated patterns
<img width="950" height="967" alt="download" src="https://github.com/user-attachments/assets/61e455ac-2dc3-4370-b5fe-47c1e1c6959b" />

3. **Name Generation**

   * Starts from `^`
   * Samples next character based on weighted probabilities
   * Stops at `$`

---

## 📦 Installation

```bash
pip install pandas networkx matplotlib
```

---

## ▶️ Usage

```python
graph = build_graph(names)

print(generate_name(graph))
```

Example output:

```
samy roberts
saran homes
roley sand
```

---

## 📊 Visualization

The graph can be visualized using NetworkX:

* Strong transitions → **thicker + darker edges**
* Weak transitions → **thin + transparent edges**

```python
visualize_graph(graph)
```

---

## 🛠️ Tech Stack

* Python 🐍
* pandas (data processing)
* networkx (graph modeling)
* matplotlib (visualization)

---

## 🔥 Future Improvements

* Higher-order Markov models (2-gram, 3-gram)
* Interactive graph visualization (web-based)
* Name style switching (fantasy, real-world, sci-fi)
* Path animation (visualizing name generation step-by-step)

---

## 📚 Concepts Used

* Markov Chains
* Graph Data Structures
* Probability & Sampling
* Data Cleaning

---

## 🤝 Contributing

Feel free to fork the project and experiment with:

* Different datasets
* Improved generation logic
* Better visualizations

---

## 📄 License

This project is open-source and available under the MIT License.

---

## 💡 Inspiration

This project demonstrates how simple probabilistic models can produce surprisingly realistic outputs — forming the foundation of more advanced AI systems.

---
