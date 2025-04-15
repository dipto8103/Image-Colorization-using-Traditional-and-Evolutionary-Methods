# Image Colorization using GANs with Hyperparameter Optimization Exploration

## Overview

This project explores the task of automatic image colorization using Generative Adversarial Networks (GANs), specifically variations of the pix2pix architecture. The primary goal is to take grayscale images as input and generate plausible colorized versions.

A key focus of this research was to **investigate and compare different hyperparameter optimization techniques**. We aimed to test the hypothesis: **Can evolutionary computation methods (like Genetic Algorithms or Ant Colony Optimization) outperform traditional methods (like Grid Search, Random Search, or Bayesian Optimization) for tuning the hyperparameters of GANs used for image colorization?**

## Core Hypothesis & Observations

* **Hypothesis:** Evolutionary hyperparameter optimization techniques can potentially find better hyperparameter configurations for complex models like GANs compared to traditional search methods, leading to improved colorization results within a comparable computational budget.
* **Observations:** Based on the experiments conducted within this project's scope, the evolutionary methods did not conclusively outperform the traditional methods. However, this outcome is potentially influenced by limitations in the training duration and computational resources available for each optimization run, even with capable hardware (like an NVIDIA RTX 4070 Super). The effectiveness of evolutionary methods often relies on extensive exploration, which might require significantly more training time than allocated here. Therefore, **the question of whether evolutionary methods can provide a definitive advantage remains open and warrants further investigation with more extensive training.**

## Features & Techniques Explored

* **Image Colorization:** Implementation of GANs (based on pix2pix) to colorize grayscale images.
* **Datasets:** Experiments conducted using datasets like Anime sketches and potentially CelebA faces (based on notebook names).
* **Hyperparameter Optimization Methods Tested:**
    * **Traditional:**
        * Grid Search
        * Random Search
        * Bayesian Optimization
    * **Evolutionary:**
        * Genetic Algorithm (GA)
        * Ant Colony Optimization (ACO) - *Exploratory*
* **Model Architecture:** Primarily focused on pix2pix-like conditional GANs.

## Technologies Used

* **Language:** Python 3.x
* **Core Libraries:**
    * PyTorch or TensorFlow (based on notebook implementations)
    * NumPy
    * Matplotlib / Seaborn (for visualization)
    * Pillow / OpenCV (for image processing)
    * Jupyter Notebook (for experimentation and visualization)
    * Libraries specific to optimization methods (e.g., scikit-optimize, or custom implementations for GA/ACO)
* **Environment Management:** `pip` and `requirements.txt`

## Project Structure

```
Image_Colorization_GAN_EC_Project/
├── research_papers/         # Relevant research papers (related work, drafts)
├── src/                     # Source code
│   ├── gan_models/          # GAN model implementations (notebooks)
│   ├── hyperparam_opt/      # Notebooks exploring different optimization methods
│   │   ├── evolutionary_method/
│   │   └── traditional_method/
│   └── utils/               # Utility scripts (dataloaders, logging, config)
├── data/                    # (Optional/Not Tracked by Git) Placeholder for datasets
├── saved_models/            # (Optional/Not Tracked by Git) Placeholder for trained models
├── requirements.txt         # Python dependencies
├── .gitignore               # Specifies intentionally untracked files by Git
└── README.md                # This file
```

## Setup and Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git) # Replace with your repo URL
    cd your-repository-name
    ```

2.  **Create a virtual environment (Recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Download Datasets:** (Add instructions here if datasets need manual download and placement, e.g., in a `data/` directory).

## Usage

The core experiments and explorations are contained within the Jupyter Notebooks (`.ipynb` files) located in the `src/` subdirectories.

1.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
2.  Navigate to the notebooks within the `src/` directory (e.g., `src/hyperparam_opt/evolutionary_method/genetic_algotithm/`) to view, run, and analyze the experiments for different models and optimization techniques.

*(Note: Training GANs, especially during hyperparameter search, can be computationally intensive and time-consuming, requiring a capable GPU like the NVIDIA RTX 4070 Super or similar.)*

## Future Work

* **Extended Training:** Conduct more extensive training runs for both traditional and evolutionary hyperparameter optimization methods to allow for more thorough exploration and potentially confirm or refute the initial hypothesis.
* **Advanced Models:** Explore more recent and advanced GAN architectures for image colorization.
* **Quantitative Evaluation:** Implement more rigorous quantitative evaluation metrics (e.g., PSNR, SSIM, FID scores) for comparing colorization results objectively.
* **Inference Service:** Develop and deploy a simple web service (using Flask/FastAPI and Docker) that uses a pre-trained model for on-demand image colorization (as part of the APD/DevOps project).
* **Refined Evolutionary Algorithms:** Further optimize the implementation and parameters of the Genetic Algorithm and ACO approaches.

## Contributing

This project was primarily developed by Dipto Sen along with Ananya Rao and Divya Athalye. Contributions, suggestions, and feedback are welcome.

Feel free to open an issue or submit a pull request.
