### Yolo2Pascal-Annotation-Conversion

Perform conversion between YOLO annotation format and Pascal VOC format. Code based on [LabelImage](https://github.com/tzutalin/labelImg) repo. Images must be in .jpg format.

### Usage:
- Convert from YOLO to Pascal annotation format: The script will search for all .txt files in the folder and perform the conversion. Converted Pascal annotation files will have the same name and in the same directory.
  - ```python3 yolo2voc.py \path\to\folder\containing\images\and\yolo\label\files```
- Convert from Pascal to Yolo annotation format: The script will search for all .xml files in the folder and perform the conversion. The script requires to have the file class.txt describing all classes (this file is generated autonomously if using the LabelImage tool above for annotating images).
  - ```python3 voc2yolo.py \path\to\folder\containing\images\and\pascal\label\files```
  - Example of class.txt file:
    - bottle
    - can
    - cup
    - glass

### TODO:
- [ ] Remove Qt dependency
- [ ] Add more on Readme
- [ ] Add support for different image formats
- [ ] Add example images
