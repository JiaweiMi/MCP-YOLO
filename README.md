

# MCP-YOLO

Custom dataset has been uploaded to the github. Available: https://github.com/JiaweiMi/MCP-YOLO.git.

The custom dataset is placed in the CustomDatatset folder, selecting the student community of a school mainly  as the shooting area, with dense small targets and mutual occlusion. The shooting time is daytime, and four categories are marked: pedestrians, electric vehicles, bicycles and cars. The dataset contains train and val, and each folder contains iamges and labels subfolders. The image is in jepg format and the label is in txt format. The whole image set consists of 335 images，and the size is 176MB.


The remaining yaml files are MCP-YOLO, other model files, and the model for ablation experiments at baseline, and the table results in letter can be obtained by training with these models.

## Directory
- [Installation Steps](#installation-steps)
- [File Directory Description](#file-directory-description)
- [Deployment environments](#deployment-environments)
- [Author](#Author)


###### **Installation Steps**

The module folder contains py files for each module, where CA.py and SEAttention.py are the referenced attention mechanisms and SwinTransformer.py is the referenced open-source Transformer module. C2S.py, MDF.py are the modules proposed in this project.
Before referencing the module, you need to copy the module proposed in this article to the ultralytics\nn\modules folder in the YOLOv8 source project, and add a reference to the module in tasks.py. It is also necessary to add parsing for the MDF and C2S modules in the parse_model function. In the parsing function, C2S is added directly to the parse_model function in the same place as the C2f and C3 modules if, while the MDF module needs to be resolved in the else if branch of parse_model as follows:



Once the installation is complete, MCP-YOLO.yaml is used for training.

### File Directory Description

MCP-YOLO 
├── CustomDataset
│  ├── train
│  │  ├── images
│  │  │  ├── image1.jpg
│  │  │  └── ...
│  │  └── labels
│  │     ├── image1.txt
│  │     └── ...
│  └──val  
│     ├── images
│     │  ├── image1.jpg
│     │  └── ...
│     └── labels
│        ├── image1.txt
│        └── ...
├── my.yaml
├── yolov5.yaml
├── yolov6.yaml
├── yolov8.yaml
├── yolov7.yaml
├── yolov9(GELANt).yaml
├── yolov10n.yaml
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


### Deployment environments

The label format is YOLO txt format. Under the Windows system, CUDA12.1+PyTorch2.2.2 environment is configured for training, and the yaml file of the training set is named my.yaml.

### Author

  Jiwei MI email: 17330356082@163.com
  Jia Liu  email: liuj2gis@163.com   




