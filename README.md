# lightningpose_utils: Utilities for the Lightning Pose Framework

**Purpose:** This package provides tools to streamline data preparation, model customization, and visualization for projects using the Lightning Pose framework.

## Prerequisites

* **lightning-pose:** Please follow the installation instructions on the Lightning Pose repository: (https://github.com/danbider/lightning-pose/tree/main)
* **Python 3.7+:** (Or adjust the Python version requirement if needed)

## Installation

```bash
git clone https://github.com/tommyly201/lightningpose_utils
cd lightningpose_utils
pip install -r requirements.txt 
pip install -e . 
```

## Overview of Modules

* **data_utils.py:** Contains data preprocessing and augmentation helpers specifically designed for Lightning Pose input formats.
* **model_utils.py:** Provides tools for easily adjusting Lightning Pose models, such as adding layers, modifying pre-trained weights, or creating custom loss functions.
* **visualization.py:** Includes functions for overlaying predicted poses on images or videos, as well as tools for qualitative error analysis.

## Basic Usage Example
```bash
python
from lightningpose_utils import data_utils, visualization
import lightning-pose as lp

# Load a sample image (adjust according to your image loading methods)
image = ... 

# Apply preprocessing suitable for Lightning Pose models
normalized_image = data_utils.normalize_for_lightningpose(image)

# Load a Lightning Pose model 
model = lp.load_model(...)

# Make predictions
predictions = model.predict(normalized_image)

# Visualize results
visualization.overlay_pose(image, predictions[0]) 
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contributing 

We welcome contributions! If you'd like to get involved, please feel free to [open an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues) or [submit a pull request](https://docs.github.com/articles/creating-a-pull-request). 

