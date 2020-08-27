### Yolo2Pascal-Annotation-Conversion

Perform conversion between YOLO annotation format and PASCAL VOC format. Code based on [LabelImage](https://github.com/tzutalin/labelImg) repo. 

### Usage:
- Images must be in .jpg format.
- YOLO to PASCAL: The script will search for all `.txt` files in the folder and perform the conversion. Converted Pascal annotation files will have the same name and in the same directory.
- PASCAL to YOLO: The script will search for all `.xml` files in the folder and perform the conversion. The script requires to have the file `class.txt` describing all classes (this file is generated autonomously if using the LabelImage tool above for annotating images).
### Demo:
 - YOLO to PASCAL:
   - ```python3 yolo2pascal/yolo2voc.py demo/yolo2pascal```
   - After this, 2 files `cat.xml` and `dog.xml` should appear in the `demo/yolo2pascal` folder. They are label files in PASCAL format. You can use LabelImage to load the directory using PASCAL format to check.
 - PASCAL to YOLO:
   - ```python3 pascal2yolo/voc2yolo.py demo/pascal2yolo```
   - After this, 2 files `cat.txt` and `dog.txt` should appear in the `demo/pascal2yolo` folder. They are label files in YOLO format. You can use LabelImage to load the directory using YOLO format to check. 
 - Example of `class.txt` file. They are just labels listed in an alphabetical order:
    - cat
    - dog

### TODO:
- [ ] Remove Qt dependency
- [ ] Add support for different image formats
