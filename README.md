# AIRL Internship Assignment

## Files in this repo
- `q1.ipynb` — Vision Transformer on CIFAR-10 (PyTorch). Run this in Google Colab with GPU.
- `q2.ipynb` — Text-driven image segmentation using SAM2. Run in Google Colab.
- `README.md` — This file.

---

## How to run (Colab)
1. Open Google Colab → File → Open notebook → GitHub tab.  
2. Paste this repo URL: `https://github.com/prajwalpruthivi/AIRL_Internship_Assignment`  
3. Select `q1.ipynb` or `q2.ipynb`.  
4. Runtime → Change runtime type → Hardware accelerator → **GPU**.  
5. Run **Runtime → Run all**.

---

## Q1 — Vision Transformer on CIFAR-10
- Model: Vision Transformer (patch size = `<patch>`, depth = `<d>`, hidden = `<h>`)  
- Training: epochs = `<E>`, batch = `<B>`, optimizer = `<optimizer>`, lr = `<lr>`  
- Best Test Accuracy (CIFAR-10): **`<xx.xx>%`**

| Model | Patch | Depth | Hidden | Best Test Acc (%) |
|-------|-------|-------|--------|------------------|
| My ViT | `<p>` | `<d>` | `<h>` | `<xx.xx>` |

*Notes:* Any extra tricks used — augmentations, scheduler, weight decay, etc.

---

## Q2 — Text-driven Image Segmentation (SAM2)
**Pipeline:** Image → text prompt / box → SAM2 → segmentation mask → overlay display.  

**How it works in this notebook:**
1. Loads SAM2 checkpoint (upload in Colab when prompted).  
2. Uses a sample image (red background with green square) for demonstration.  
3. SAM2 predicts the mask automatically and displays overlay.  

**Limitations:** Works for single images; requires GPU for faster execution; SAM2 checkpoint must be provided.

---

## Notes
- Both notebooks are runnable end-to-end in Colab with GPU.  
- If anything fails, restart runtime and run all cells again.
