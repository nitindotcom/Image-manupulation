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



