---
license: mit
task_categories:
- text-classification
- text-generation
language:
- en
tags:
- code
pretty_name: '*'
size_categories:
- 0.001M<n<0.0011M
---

# mini coco dataset files

Hugging Face Link: https://huggingface.co/datasets/iix/mini_coco_linux

# Required dependencies 

```
OpenCV (cv2)

matplotlib

ipywidgets
```


# img_data.psv

Extract of the coco dataset containing the following labels: ```["airplane", "backpack", "cell phone", "handbag", "suitcase", "knife", "laptop", "car"]```  (300 of each)

```
Structured as follows:

| Field           | Description                                                                                         |
| --------------- | --------------------------------------------------------------------------------------------------- |
| file_name       | Name of image file (.png)                                                                           |
| height          | Image height prior to padding                                                                       |
| width           | Image width prior to padding                                                                        |
| annotations     | Array of boundary box array, label pairs. Bbox arrays are of the form [x_min, y_min, width, height] |

1.09k rows
```


# /data (folder)

This directory contains a selection of zero-padded COCO images that correspond to img_data.parquet, image names are of the following format:
```
xxxxxx.png
```


# display_boundary.py

Allows images to be viewed with their boundary boxes, don't need to pay attention to how it works.

```
- Intended to run in tandem with jupyter notebook. 

- Takes img_name.png as input, inspect img_data.psv or /data for image names.

```


If you have any questions or issues, feel free to keep them to yourself.