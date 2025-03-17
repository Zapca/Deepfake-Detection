# Pix2Pix GAN for Image Colorization

This repository contains a pre-trained pix2pix GAN model for colorizing grayscale images.

## Setup

Make sure you have the required dependencies installed:

```bash
pip install tensorflow tensorflow-addons opencv-python numpy matplotlib pillow
```

## Using the Colorization Script

The `colorize_personal_images.py` script provides an easy way to colorize your personal images using the pre-trained model.

### Colorize a Single Image

```bash
python colorize_personal_images.py --image path/to/your/image.jpg
```

This will display the original, grayscale, and colorized versions of your image.

### Colorize and Save a Single Image

```bash
python colorize_personal_images.py --image path/to/your/image.jpg --save
```

The colorized image will be saved in the `colorized_outputs` directory.

### Colorize Multiple Images from a Directory

```bash
python colorize_personal_images.py --directory path/to/your/images/folder
```

### Colorize and Save Multiple Images

```bash
python colorize_personal_images.py --directory path/to/your/images/folder --save --output_dir your_output_folder
```

## Model Details

This is a pix2pix conditional GAN for image colorization. The architecture includes:

- Generator: U-Net based architecture
- Discriminator: PatchGAN with multiple scales
- Training data: Landscape images

The model was trained on pairs of grayscale and colored images.

## Examples

To test the model with the provided examples, run:

```bash
python colorize_personal_images.py --directory archive\ \(3\)/landscape\ Images/gray --save
```

This will colorize the example grayscale images from the training dataset.

## Using the Jupyter Notebook

If you prefer to use the Jupyter notebook:

1. Open the `pix2pix-gan-for-image-colourisation.ipynb` notebook
2. Run all the needed cells
3. At the end of the notebook, add cells similar to the Python script to process your personal images 
