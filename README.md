# Image Captioning + GenZ/Brainrot Rewriter

A chaotic little deep-learning project that does two things:

1. Generates image captions using an attention-based encoder-decoder model.
2. Rewrites those captions into GenZ / terminally-online internet slang.

Because apparently "a dog running through grass" is less important than  
"bro is absolutely zoomin fr fr".

---

## Features

- Attention-based image captioning model
- Uses `InceptionResNetV2` as image encoder
- GRU decoder with Luong-style attention
- Trained on a subset of the COCO captions dataset
- Top-K sampling for varied caption generation
- GenZ / brainrot text rewriting pipeline
- Upload-your-own-image demo
- Optional model save & reload support

---

## Model Architecture

```text
Image
  ↓
InceptionResNetV2 Encoder (ImageNet pretrained)
  ↓
Attention Layer
  ↓
GRU Decoder
  ↓
Generated Caption
  ↓
GenZ / Brainrot Rewriter
```

Classic encoder-decoder setup.  
Just with more internet damage.

---

## Notebook Contents

| Section | Description |
|---|---|
| Dataset Loading | Loads and preprocesses COCO captions |
| Tokenisation | Cleans and tokenises captions |
| Dataset Pipeline | Builds TensorFlow training datasets |
| Model Building | Encoder + attention + GRU decoder |
| Training | Trains caption generation model |
| Inference | Stateful prediction pipeline |
| Caption Rewriting | Converts captions into GenZ slang |
| Demo | Run predictions on uploaded images |

---

## Example

### Normal Caption
```text
a dog running through a grassy field
```

### GenZ / Brainrot Version
```text
bro is zoomin through the grass no cap
```

The model uses probabilistic sampling, so outputs vary between runs.

---

## Tech Stack

- Python
- TensorFlow / Keras
- TensorFlow Datasets
- NumPy
- Matplotlib
- Pillow

---

## Installation

```bash
pip install tensorflow tensorflow-datasets keras pillow
```

---

## Running the Notebook

Open the notebook and run the cells sequentially.

```bash
jupyter notebook image_captioning_genz.ipynb
```

or use Google Colab / Kaggle.

---

## Dataset

This project uses the COCO Captions dataset through TensorFlow Datasets.

Dataset source:

- https://cocodataset.org/

---

## Notes

- The notebook is designed more for experimentation and learning than production deployment.
- Training on larger dataset slices and longer epochs will significantly improve caption quality.
- The GenZ rewriter is intentionally unserious. The model itself is not. Mostly.
