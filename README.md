### Yolo2Pascal-Annotation-Conversion

Perform conversion between YOLO annotation format and PASCAL VOC format and vice versa. Code based on [LabelImage](https://github.com/tzutalin/labelImg) repo. 

### Usage:
- Images must be in .jpg/.png format.
- YOLO to PASCAL: The script will search for all `.txt` files in the folder and perform the conversion. Converted PASCAL annotation files have a `.xml` extension, reside in the same folder and share the same name with their corresponding images.
- PASCAL to YOLO: The script will search for all `.xml` files in the folder and perform the conversion. The script requires a file `class.txt` describing all classes (this file is generated autonomously if using the LabelImage tool above for annotating images). Converted YOLO annotation files have a `.txt` extension, reside in the same folder and share the same name with their corresponding images.
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
- [x] Add support for different image formats (thanks [guysoft](https://github.com/guysoft/guysoft))
