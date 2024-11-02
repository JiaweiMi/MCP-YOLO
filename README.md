

# MCP-YOLO

Custom dataset has been uploaded to the github. Available: https://github.com/JiaweiMi/MCP-YOLO.git

The custom dataset is placed in the CustomDatatset folder, selecting the student community of a school mainly  as the shooting area, with dense small targets and mutual occlusion. The shooting time is daytime, and four categories are marked: pedestrians, electric vehicles, bicycles and cars. The dataset contains train and val, and each folder contains iamges and labels subfolders. The image is in jepg format and the label is in txt format. The whole image set consists of 335 images, and the size is 176MB.


The remaining yaml files are MCP-YOLO, other model files, and the model for ablation experiments at baseline, and the table results in letter can be obtained by training with these models.

## Directory
- [Installation Steps](#installation-steps)
- [File Directory Description](#file-directory-description)
- [Deployment environments](#deployment-environments)
- [Author](#Author)


### Installation Steps


### File Directory Description

```
MCP-YOLO 
├── CustomDataset
│  ├── train
│  │  ├── images
│  │  │  ├── image1.jpg
│  │  │  └── ...
│  │  └── labels
│  │     ├── image1.txt
│  │     └── ...
│  ├──val  
│  │  ├── images
│  │  │  ├── image1.jpg
│  │  │  └── ...
│  │  └── labels
│  │     ├── image1.txt
│  │     └── ...
│  ├── my.yaml
│  ├── yolov5.yaml
│  ├── yolov6.yaml
│  ├── yolov8.yaml
│  ├── yolov7.yaml
│  ├── yolov9(GELANt).yaml
│  └── yolov10n.yaml
├── MCP-YOLO
│  ├── yolov8+C2S.yaml
│  ├── yolov8+MDF.yaml
│  ├── yolov8+p2.yaml
│  └── MCP-YOLO.yaml
└── module
   ├── C2S.py
   ├── MDF.py
   ├── CA.py
   ├── SwinTransformer.py
   └── SEAttention.py

```
### Deployment environments

The label format is YOLO txt format. Under the Windows system, CUDA12.1+PyTorch2.2.2 environment is configured for training, and the yaml file of the training set is named my.yaml.

### Author

Jiwei MI email: 17330356082@163.com
Jia Liu  email: liuj2gis@163.com   




