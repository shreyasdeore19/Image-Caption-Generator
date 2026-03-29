# Flickr8k Image Captioning (CNN + LSTM)

**Repository:** [github.com/shreyasdeore19/Image-Caption-Generator](https://github.com/shreyasdeore19/Image-Caption-Generator)

```bash
git clone https://github.com/shreyasdeore19/Image-Caption-Generator.git
```

Minimal repository: a **Jupyter notebook** that trains/evaluates an image captioning model on **Flickr8k**, plus a **saved Keras model** for inference or reuse.  
Course context: **Topics in Machine Learning** — encoder (CNN image features) + decoder (LSTM) with **BLEU** evaluation (NLTK).

---

## What’s in this repository

| File | Description |
|------|-------------|
| **`Image Caption Generator - Flickr Dataset - CNN-LSTM.ipynb`** | End-to-end Flickr8k CNN–LSTM captioning notebook (VGG16-style image features + LSTM). |
| **Trained model** (`.keras` or `.h5`) | Saved Keras model; use the same filename in `tf.keras.models.load_model(...)` (or equivalent) inside the notebook. |
| **`README.md`** | This file. |

**Suggested GitHub layout (minimal upload):** put the notebook, your model file, and `README.md` in the **repository root** so paths stay simple. If you keep a nested folder (e.g. `flickr8k notebook/...`), update any hard-coded paths in the notebook accordingly.

---

## Dataset (download separately)

The notebook is built for **Flickr8k**: 8,000 images and **five captions per image**. The images and captions are **not** included in this repo — download them yourself and point the notebook to your local paths.

| Resource | Link |
|----------|------|
| **Flickr8k on Kaggle** (images + `captions.txt`) | [kaggle.com/datasets/adityajn105/flickr8k](https://www.kaggle.com/datasets/adityajn105/flickr8k) |

**How to cite the data (paper):**  
M. Hodosh, P. Young, J. Hockenmaier, *Framing Image Description as a Ranking Task: Data, Models and Evaluation Metrics*, Journal of Artificial Intelligence Research, 2013.  
(Also search “Flickr8k dataset paper” for the official reference your course prefers.)

**Terms:** Use of Flickr8k is subject to the **dataset / Kaggle license** and any course rules; do not redistribute the raw images on GitHub if the license forbids it.

---

## Requirements

- Python 3.x  
- **TensorFlow** / **Keras**  
- **NumPy**, **pandas**, **matplotlib**, **PIL** (Pillow)  
- **NLTK** (e.g. for BLEU)  
- **tqdm**  

The notebook metadata indicates it was run on **Kaggle** with GPU; for local runs, update paths (data root, saved model path) to match your machine.

---

## How to use

1. Download **Flickr8k** from Kaggle (link above) and unzip.  
2. Clone this repo and open **`Image Caption Generator - Flickr Dataset - CNN-LSTM.ipynb`**.  
3. Set variables/paths in the notebook to your **Images** folder and **captions** file.  
4. Place your **Keras** file where the notebook expects it, or edit the load/save cells to use your filename (e.g. `model.keras`).  
5. Run cells in order (training) or jump to inference if the notebook supports loading the saved model only.

---

## Results (reference)

Example BLEU scores reported for a CNN–LSTM setup on this task (exact values depend on split and training):

| Metric | Flickr8k (example) |
|--------|---------------------|
| BLEU-1 | ~0.54 |
| BLEU-2 | ~0.32 |

---

## License

Code/notebook: suitable for **educational / coursework** use; add a `LICENSE` file if you want to specify reuse (e.g. MIT).  
**Dataset:** follow [Kaggle Flickr8k](https://www.kaggle.com/datasets/adityajn105/flickr8k) and the original dataset terms.
