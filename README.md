# Prompt2Animate | Stable Diffusion Model using PyTorch

## Overview

This repository contains a PyTorch implementation of a stable diffusion model from scratch. The diffusion model is a powerful probabilistic generative model that has applications in image synthesis, denoising, and other tasks.

![Stable Diffusion](assets/diffusion.jpg)

## Features

- **PyTorch Implementation:** The diffusion model is implemented using PyTorch, providing flexibility and ease of use for both training and inference.

- **Stability:** The implementation ensures stability during training, allowing for reliable convergence and generation of high-quality samples.

- **Customization:** Easily adapt the model to different datasets and tasks by customizing the architecture and hyperparameters.

## Getting Started

### Prerequisites

- Python 3.x
- PyTorch (>=1.7.0)
- Additional dependencies (specified in `requirements.txt`)

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/deepak7376/Prompt2Animate.git
    cd Prompt2Animate
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Download the pre-trained weights
    ```bash
    wget -O saved_models/v1-5-pruned-emaonly.ckpt https://huggingface.co/runwayml/stable-diffusion-v1-5/resolve/main/v1-5-pruned-emaonly.ckpt
    ```

### Usage

1. Inference (Text-to-image):

    ```bash
    python src/inference.py --prompt "photograph of an astronaut riding a horse"
    ```
    ![Text-to-image](assets/txt-to-img.jpg)

2. Inference (Image-to-image):

    ```bash
    python src/inference.py --prompt "Put hat on the cat head, ultra-sharp, cinematic, 100mm lens, 8k resolution." --image-path="cat.jpg"
    ```
    ![Image-to-image](assets/img-to-img.jpg)

## Structure

- **`src/`**: Contains the source code for the diffusion model implementation.
- **`data/`**: Placeholder for your dataset or data loading scripts.
- **`saved_models/`**: Directory to store trained model checkpoints.

## Future Work

- **Implement Training Strategies:** To train diffusion model on custom dataset.

- **Parallelization and Optimization:** Investigate opportunities for parallelizing training and optimizing the code for faster convergence on different hardware configurations.

- **Quantization:** Qauntize the model for faster inference time


## Contributing

If you find any issues or have suggestions for improvement, feel free to open an issue or create a pull request. Contributions are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- Inspired by the work of [Umar Jamil YouTube Video](https://www.youtube.com/watch?v=ZBKpAp_6TGI&t=12146s).
