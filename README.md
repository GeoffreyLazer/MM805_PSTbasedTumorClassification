# MM805 Project – PhyCV-Based Brain Tumor Enhancement

This notebook demonstrates the use of the **Phase Stretch Transform (PST)** algorithm, implemented using the [PhyCV](https://github.com/phycom/phycv) library, to enhance brain tumor MRI images.

## 📁 Files

- `MM_805_Project.ipynb`: Main notebook that runs PST on MRI brain scan images.
- Input Image: Assumes access to an image path in Google Drive (e.g., `/content/drive/Shareddrives/Test/Brain-Tumor-Detection-master/yes/Y10.jpg`)
- Output: Saved enhanced image as `PST_CPU_compare.jpg`.

## 🚀 Quick Start (Google Colab)

1. **Open in Google Colab**:  
   Upload the notebook or use:  
   [Open in Colab](https://colab.research.google.com)

2. **Install Required Libraries**:

```python
!pip install phycv opencv-python numpy
!pip install av imageio imageio-ffmpeg kornia matplotlib Pillow torch torchvision
```

3. **Mount Google Drive**:

```python
from google.colab import drive
drive.mount('/content/drive')
```

4. **Run the Notebook**:
   - Set the correct image path in the `img_file` variable.
   - Run all cells to generate and visualize PST-enhanced outputs.

## ⚙️ PST Parameters

The PST algorithm is applied using the following tunable parameters:

- `S`: Strength of the PST kernel
- `W`: Warp strength
- `sigma_LPF`: Low-pass filter sigma
- `thresh_min`, `thresh_max`: Thresholding values
- `morph_flag`: Whether to apply morphological processing

## 📊 Output

Enhanced images are saved in the `./output/` directory. Visualization includes:

- Original image
- PST-enhanced result using CPU (and optionally GPU if available)

## 📌 Notes

- Ensure the image path points to a valid file in your Google Drive.
- The notebook will fall back to CPU if GPU is unavailable.
