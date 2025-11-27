# ContrastiveLanguageImagePreTraining

Educational notebooks for working with **CLIP**  
(Contrastive Language–Image Pre-Training) using **PyTorch** and **transformers**.

This repository currently contains two Jupyter notebooks that demonstrate how to:

- Build **text and image embeddings** with CLIP
- Compare similarities between texts, images, and text–image pairs
- Perform **Zero-Shot Image Classification** (no task-specific training)

---

## Repository Structure

- `CLIP_Embeddings.ipynb`  
  Work with CLIP embeddings for text and images:
  - Generate **text embeddings** for different prompts
  - Generate **image embeddings** from example images
  - Compute **cosine similarity**:
    - between text prompts  
    - between images  
    - between text and images
  - Visualize similarities with **heatmaps** using `matplotlib` and `seaborn`
  - Key concepts: tokenization, text embedding, image embedding, cosine similarity

- `Zero-Shot-Classification-CLIP.ipynb`  
  Zero-shot image classification with CLIP:
  - Load pre-trained CLIP model and processor (`CLIPModel`, `CLIPProcessor`)
  - Define a set of **text labels** (e.g. `"a cat"`, `"a donut"`, `"an airplane"`)
  - Compute image–text similarity scores (**logits**)
  - Convert logits to probabilities using **softmax**
  - Select the most probable label as the **predicted class**
  - Key concepts: logits, temperature / logit scale, softmax, zero-shot prediction

---

## Requirements

- Python **3.8+**
- Jupyter Notebook / JupyterLab / VS Code (with Jupyter extension)
- Python packages:

```bash
pip install torch torchvision torchaudio      # or CPU-only build based on your system
pip install transformers matplotlib seaborn numpy pillow requests
