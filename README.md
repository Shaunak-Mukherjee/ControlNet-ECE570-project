# ControlNet ECE570 Project 🚀

> A PyTorch‑powered ControlNet implementation on MNIST for ECE 570 final term.  
> Unconditional DDPM baseline + ControlNet conditioning on Canny edges.  

---

## 🔍 Overview
This is my final term project for _ECE 570_—we dive into diffusion models by:
1. Training an **Unconditional DDPM** on MNIST  
2. Extending it with **ControlNet** that uses Canny‑edge hints  

Everything’s wrapped in a Colab notebook (`Main_mnist.ipynb`) with step‑by‑step cells. Let’s get those 🔥 handwritten digits!

---

## 📁 Directory Structure
```
├── config/
│   └── mnist.yaml          # DDPM + ControlNet hyperparams
├── data/
│   └── mnist/
│       ├── train/images    #   <– put your Kaggle MNIST here
│       └── test/images
├── mnist/                  # helper scripts (if any)
├── Main_mnist.ipynb        # 🎓 Colab tutorial & all-in-one notebook
├── requirements.txt        # pip deps
├── ControlNet_Cannyedge_genimage.png  # sample output
├── controlnet_time_evolution.mp4      # cool time‑evo vid
├── ECE570_final_term_paper_ControlNet-ECE570-D5C5_v3.pdf  # report
└── unet_model_graph.png    # U‑Net arch diagram
```

---

## ⚙️ Installation

1. **Clone this repo**
   ```bash
   git clone https://github.com/Shaunak-Mukherjee/ControlNet-ECE570-project.git
   cd ControlNet-ECE570-project
   ```
2. **(Colab only) Set up Conda**  
   ```python
   %pip install condacolab
   import condacolab
   condacolab.install()
   ```
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

---

## 📦 Data Preparation

1. Download MNIST from [Kaggle: hojjatk/mnist-dataset][kaggle-mnist].  
2. Organize files as:
   ```
   data/mnist/train/images/*/*.png
   data/mnist/test/images/*/*.png
   ```

---

## 🔧 Configuration

Tweaks for model size, learning rate, timesteps, etc., live in `config/mnist.yaml`. Play around to see how your samples change! 😎

---

## 🎬 Usage

1. Open **Main_mnist.ipynb** in Google Colab.  
2. Run cells in order:
   - Install & import libs  
   - Load + preprocess MNIST  
   - Train **Unconditional DDPM**  
   - Train **ControlNet** (Canny‑edge hints)  
   - Sample & visualize results  

All generated images & checkpoints will be dumped under `mnist/samples/` & `mnist/` folders.

---

## 🌟 Results

- **Canny‑edge control samples** ➡️ `ControlNet_Cannyedge_genimage.png`  
- **Time‑evolution video** ➡️ `controlnet_time_evolution.mp4`  

Check ’em out and flex your synthetic digits! 😉

---

## 🤝 Contributing

Love it? Spot a bug? PRs & issues are welcome! Let’s collab. 💡

---

## 📄 License

MIT © 2025 Shaunak Mukherjee

---

## 📬 Contact

Shaunak Mukherjee – (https://www.linkedin.com/in/shaunakmukherjee/)
_P.S. Replace above with your real email so folks can reach you!_  

---

[kaggle-mnist]: https://www.kaggle.com/datasets/hojjatk/mnist-dataset
