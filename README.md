# Vintage-Packaging-ML-Classification

## Project Description:

### Overview

How can we make packaging more sustainable? This is a common question in today's world, and many people would tell you the solution is innovation whether that be through biodegradable plastics or training worms to eat styrofoam. These people are looking to the future, but what if the key to our sustainability issues can be found in the past? Humanity has thrived without plastics up until the industrial era. Maybe the question we need to ask is not how can we make plastic more environmentally friendly, rather, how can we switch back to the plastic free market that we once had? Was the past more sustainable? This project will analyze images from vintage grocery stores to do two things. Firstly we will analyze if the past was actually more sustainable, and two how we can implement these practices in today's world. How can we learn from the past to improve our sustainability today? What was common sustainable packaging during the pre-industrial era, and has since been lost in favor of plastics?

### Research question

Can machine learning identify the materials used in historical images of grocery stores and markets, and what information about sustainable packaging can we take away from the past to improve our future?

### Datasets

1. Vintage Grocery Store (VGS) dataset: 50 hand-labeled historical grocery store images (3186 annotations) with 9 classes: glass, metal, paper, plastic, wood, wicker, linen, ceramic, mesh. Available on Roboflow (Link can be found below).
2. Modern Packaging (MP) dataset: 1491 images of modern packaging (1491 annotations) converted to greyscale and enhanced exposure to mimic historical images. 4 classes: glass, metal, paper, plastic. Available on Roboflow (Link can be found below).

### Experiments Conducted:

Experiment 1. Transfer learning with YOLOv5 w/Pytorch using only VGS dataset for fine tuning. Glass showed the most promise. (Full data can be found in VGS data spreadsheet).

Experiment 2. Transfer learning with YOLOv12 w/Pytorch using only VGS dataset for fine tuning. Wood and glass showed the most promise. (Full data can be found in VGS data spreadsheet).

Experiment 3. Transfer learning with YOLOv12 w/Pytorch using only MP dataset for fine tuning and tested using VGS dataset. Plastic showed the most promise. (Full data can be found in VGS data spreadsheet).

Experiment 4. (Not yet completed) Transfer learning with YOLOv12 w/Pytorch using both VGS and MP dataset for fine tuning.


### Key findings

Packaging classification on historical images is extremely difficult even with newer machine learning models. Due to the exposure and greyscale of most historical images, it is hard for the machine to differentiate metal and glass as the only differences are in shape. This is doable however, with a more expansive dataset the accuracy will improve.

Using the modern dataset is not a great solution to the previous issue of a smaller dataset. Due to the large number of plastic packaging in most datasets it creates a bias in the machine, this can be seen in VGS3w_YOLOv11. 

### Tools used

- YOLOv11 and YOLOv5 via Ultralytics
- Roboflow for labeling and dataset managment
- Google colab for training using T4 GPU

### Next steps:

- Expand VGS dataset to 200+ images
- Create or remove class imbalance in MP dataset
- Use quantitative data from machine learning to research what information about sustainable packaging can be taken away from the past to improve our future?

## Roboflow datasets:

**Access to Roboflow project workspace**:
https://app.roboflow.com/join/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ3b3Jrc3BhY2VJZCI6IlFQZm16cEJCTGNWUk03M25CTnRqVElYT3dDRzMiLCJyb2xlIjoib3duZXIiLCJpbnZpdGVyIjoicm9ocmVjQGR1a2VzLmptdS5lZHUiLCJpYXQiOjE3ODQxOTczODV9.ARGds_18c7TUkf-G1dESodb3KnGc-3TjHibdApgXKLM
___________________________________________________________________________________________________________________________________________
**Vintage grocery store labeled images dataset**: https://universe.roboflow.com/ellas-workspace-yh4lc/vintage-grocery-store-packaging-dkarf

**Cite**:
@misc{ vintage-grocery-store-packaging-dkarf_dataset,
  title = { vintage-grocery-store-packaging Dataset },
  type = { Open Source Dataset },
  author = { Ellas Workspace },
  howpublished = { \url{ https://universe.roboflow.com/ellas-workspace-yh4lc/vintage-grocery-store-packaging-dkarf } },
  url = { https://universe.roboflow.com/ellas-workspace-yh4lc/vintage-grocery-store-packaging-dkarf },
  journal = { Roboflow Universe },
  publisher = { Roboflow },
  year = { 2026 },
  month = { jul },
  note = { visited on 2026-07-16 },
}

___________________________________________________________________________________________________________________

**Plastic, glass, metal, and paper dataset**: https://universe.roboflow.com/example-wg2gf/plastic-glass-metal-paper

**Cite**:
@misc{ plastic-glass-metal-paper_dataset,
  title = { plastic-glass-metal-paper Dataset },
  type = { Open Source Dataset },
  author = { example },
  howpublished = { \url{ https://universe.roboflow.com/example-wg2gf/plastic-glass-metal-paper } },
  url = { https://universe.roboflow.com/example-wg2gf/plastic-glass-metal-paper },
  journal = { Roboflow Universe },
  publisher = { Roboflow },
  year = { 2025 },
  month = { jul },
  note = { visited on 2026-07-16 },
}

