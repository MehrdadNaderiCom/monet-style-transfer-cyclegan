# Monet Style Transfer Using CycleGAN 🎨

This repository contains a CycleGAN-based project to perform style transfer, transforming real-world photos into Monet-style paintings. Developed using TensorFlow, this project demonstrates the power of Generative Adversarial Networks (GANs) in image-to-image translation tasks.

---

## **Project Overview**

The goal of this project is to generate Monet-style paintings from real-world photos. By training a CycleGAN model, we achieve high-quality style transfer using a dataset containing Monet paintings and real photos.

---

## **Dataset**

The dataset used for this project is from the Kaggle competition [I'm Something of a Painter Myself](https://www.kaggle.com/c/gan-getting-started). It includes:
- **Monet paintings:** 300 images
- **Real-world photos:** 7,038 images

---

## **Directory Structure**

The repository is organized as follows:

> notebooks/
> - Monet_Style_Transfer.ipynb  # Main Jupyter notebook for the project
>
> images/
> - images.zip
>
> README.md                     # Project overview and instructions

---

## **Key Features**
- **Preprocessing:** Normalized datasets to [-1, 1] for stable GAN training.
- **Model Architecture:**
  - **Generators:** U-Net-based architecture with residual blocks.
  - **Discriminators:** PatchGAN architecture.
  - **Losses:** Adversarial, Cycle-Consistency, and Identity Losses.
- **Training:**
  - Mixed precision for faster training.
  - Optimized using Adam optimizers with `learning_rate=2e-4` and `beta_1=0.5`.
  - Trained for 10 epochs using TensorFlow on a GPU-enabled environment.
- **Evaluation:**
  - MiFID (Memorization-informed Fréchet Inception Distance) for quality assessment.
  - Visualized results showcasing real-photo to Monet-style transformations.

---

## **Setup and Usage**

### **Requirements**
- Python 3.7+
- TensorFlow 2.x
- Matplotlib, NumPy, Pandas

### **Steps to Run**
1. Clone the repository:
    ```bash
    git clone https://github.com/<your-username>/monet-style-transfer-cyclegan.git
    cd monet-style-transfer-cyclegan
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download the dataset using the Kaggle API:
    ```bash
    kaggle competitions download -c gan-getting-started
    unzip gan-getting-started.zip -d data/
    ```

4. Run the notebook:
    ```bash
    jupyter notebook
    ```

5. Open the notebook `Monet_Style_Transfer.ipynb` and execute cells sequentially.

---

## **Future Improvements**
- Fine-tuning model hyperparameters for better output quality.
- Increasing training epochs for improved consistency.
- Experimenting with other GAN architectures like Pix2Pix for comparison.

---

## **Acknowledgements**
- **Dataset:** Kaggle [I'm Something of a Painter Myself](https://www.kaggle.com/c/gan-getting-started).
- **Frameworks:** TensorFlow, NumPy, Matplotlib.

---

## **Contact**
For questions or feedback, feel free to contact:
- **Name:** Mehrdad Naderi
- **Email:** mail@mehrdadnaderi.com
- **GitHub:** [MehrdadNaderiCom](https://github.com/MehrdadNaderiCom)
