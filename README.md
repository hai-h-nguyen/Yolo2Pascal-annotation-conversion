### Yolo2Pascal-Annotation-Conversion

Perform conversion between YOLO annotation format and Pascal VOC format. Code based on [LabelImage](https://github.com/tzutalin/labelImg) repo. Images must be in .jpg format.

### Usage:
- Convert from YOLO to Pascal annotation format: The script will search for all .txt files in the folder and perform the conversion. Converted Pascal annotation files will have the same name and in the same directory.
  - ```python3 yolo2voc.py \path\to\folder\containing\images\and\yolo\label\files```
- Convert from Pascal to Yolo annotation format: The script will search for all .xml files in the folder and perform the conversion. The script requires to have the file class.txt describing all classes (this file is generated autonomously if using the LabelImage tool above for annotating images). One example of this file can be seen at https://github.com/tzutalin/labelImg/blob/master/data/predefined_classes.txt
  - ```python3 voc2yolo.py \path\to\folder\containing\images\and\pascal\label\files```
 ### Demo:
 - Convert from YOLO to Pascal:
 - ```python3 yolo2pascal/yolo2voc.py demo/yolo2pascal```
 After this, 2 files `cat.xml` and `dog.xml` should appear in the `demo/yolo2pascal` folder. They are label files in Pascal format. You can use LabelImage to load the directory using Pascal format to check.
 - Convert from Pascal to Yolo:
 - ```python3 pascal2yolo/voc2yolo.py demo/pascal2yolo```
 After this, 2 files `cat.txt` and `dog.txt` should appear in the `demo/yolo2pascal` folder. They are label files in Pascal format. You can use LabelImage to load the directory using YOLO format to check. 
 - Example of class.txt file. They are just labels sorted in an alphabetical order:
    - cat
    - dog

### TODO:
- [ ] Remove Qt dependency
- [ ] Add support for different image formats
