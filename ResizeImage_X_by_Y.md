# Image Resizer

This Python script resizes an existing image to multiple sizes using the Pillow library.

## Prerequisites

- Python 3.x
- Pillow library

## Installation

1. Install Python 3.x from the official [Python website](https://www.python.org/).

2. Install the Pillow library using pip:

   ```sh
   pip install Pillow

## Usage

1. Clone or download this repository to your local machine.

2. Place the image you want to resize in the same directory as the script. Update the script with the correct filename if necessary.

3. Run the script to resize the image to 120x120, 48x48, and 16x16 pixels.

   ```sh
   python resize.py

## Script Details

### resize.py

```python
from PIL import Image

# Open an existing image
image = Image.open('your_image.png')

# Define the new sizes
sizes = [(120, 120), (48, 48), (16, 16)]

# Loop over each size and save the resized image
for size in sizes:
    resized_image = image.resize(size, Image.LANCZOS)
    resized_image.save(f'resized_image_{size[0]}x{size[1]}.png')

print("Images have been resized and saved successfully.")


##Explanation

- **Image.open('your_image.png')**: Opens the existing image. Replace 'your_image.png' with the path to your image file.
- **sizes**: A list of tuples specifying the desired sizes (120x120, 48x48, 16x16).
- **image.resize(size, Image.LANCZOS)**: Resizes the image using the LANCZOS filter for high-quality downsampling.
- **resized_image.save(f'resized_image_{size[0]}x{size[1]}.png')**: Saves the resized image with a new filename that includes the size.

## Output

The script will create three resized images in the same directory:

- `resized_image_120x120.png`
- `resized_image_48x48.png`
- `resized_image_16x16.png`


