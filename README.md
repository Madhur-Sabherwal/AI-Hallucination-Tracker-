

# AI Hallucination Tracker (Client-Side)

## 📌 Overview

The **AI Hallucination Tracker** is a **single-file HTML web application** that runs entirely in your browser — no server, no backend, no data leakage.
It compares AI model outputs against ground truth datasets to calculate accuracy metrics, detect hallucinations, and generate visual leaderboards.

Built with a **warm gradient theme** and **animated ember effects**, it’s both functional and visually engaging.

---

## ✨ Features

* **Client-Side Processing** – Your data never leaves your machine.
* **CSV Upload** – Load your own *Ground Truth* and *Predictions* files.
* **Multiple Metrics** – Exact Match, Token-F1, ROUGE-L (Longest Common Subsequence).
* **Hallucination Detection** – Flags long, incorrect responses.
* **Visual Leaderboard** – Per-model performance at a glance.
* **Error Buckets** – See where each model fails most.
* **Row-Level Explorer** – Drill down into specific cases.
* **CSV Export** – Download processed results for reporting.
* **Stylized UI** – Warm color palette with animated embers.

---

## 📂 File Structure

```
index.html   → Main single-page app
README.md    → This documentation
```

---

## 🛠 How to Use Locally

1. **Download** `index.html` from this repo.
2. Double-click to open it in your browser.
3. Click **Upload Ground Truth CSV** and **Upload Predictions CSV**.

   * Ground Truth CSV format:

     ```
     id,question,answer
     1,What is the capital of France?,Paris
     ```
   * Predictions CSV format:

     ```
     id,model,output
     1,Model A,Paris
     ```
4. Review metrics, explore flagged hallucinations, and export results.

---

## 🌍 Deploy to GitHub Pages

1. Create a **public repository** on GitHub.
2. Upload `index.html` to the **root** of your repo.
3. Commit & push changes.
4. Go to **Settings → Pages**.
5. Under *Branch*, select `main` (or your default branch) and `/ (root)`.
6. Save and wait \~1–2 minutes for deployment.
7. Access your live app via the GitHub Pages URL provided.

---

## 📊 Metrics Explained

* **Exact Match (EM)** – 1 if output matches exactly, 0 otherwise.
* **Token-F1** – Harmonic mean of precision and recall over token overlap.
* **ROUGE-L** – Measures longest common subsequence between output and ground truth.
* **Composite Score** – Weighted combination of the above metrics.

---

## ⚙️ Customization

* Edit **metric weights** in the JavaScript section to adjust scoring.
* Change **hallucination threshold** to tune sensitivity.
* Modify **CSS variables** to tweak colors, embers, or background.

---

## 📜 License

This project is released under the MIT License — you’re free to use, modify, and distribute.
