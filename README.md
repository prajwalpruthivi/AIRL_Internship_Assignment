# AIRL Internship Assignment

## Files in this repo
- `q1.ipynb` — Vision Transformer on CIFAR-10 (PyTorch). Run this in Google Colab with GPU.
- `q2.ipynb` — Text-driven image segmentation using SAM2. Run in Google Colab.
- `README.md` — This file.

---

## How to run (Colab)
1. Open Google Colab → File → Open notebook → GitHub tab.  
2. Paste this repo URL: `https://github.com/prajwalpruthivi/AIRL_Internship_Assignment`  
   and open `q1.ipynb` or `q2.ipynb`.  
3. Runtime → Change runtime type → Hardware accelerator → **GPU**.  
4. Run **Runtime → Run all**.

---

## Q1 — Vision Transformer on CIFAR-10

**Best Model Configuration & Results:**
| Model | Patch | Depth | Hidden | Best Test Acc (%) |
|-------|-------|-------|--------|------------------|
| My ViT | 4     | 6     | 128    | 65.32            |

**Notes / Bonus Analysis:**
- Used RandomCrop + HorizontalFlip for augmentation.
- AdamW optimizer, cosine annealing LR scheduler.
- Increasing depth/hidden size improves accuracy but increases GPU time.
- Optional tricks: Cutout, Mixup, larger batch sizes may improve results further.

---

## Q2 — Text-driven Image Segmentation (SAM2)

**Pipeline:**
1. Upload an image.
2. Provide a text prompt for the object to segment.
3. Convert text to region seeds using GroundingDINO/CLIPSeg.
4. Feed seeds to SAM2 → get segmentation mask.
5. Overlay mask on the image and display.

**Limitations:**
- Only works on single images.
- Requires SAM2 checkpoint file.
- Heavy GPU memory usage for large images.
- Ambiguous text prompts may fail.

---

## Notes
- Both notebooks are runnable end-to-end on Colab (GPU).  
- If anything fails, restart runtime and run all cells again.
