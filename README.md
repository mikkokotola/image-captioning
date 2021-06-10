# Architectures of Leading Image Captioning Systems
MSc thesis "Architectures of Leading Image Captioning Systems" at the University of Helsinki Master's Programme in Data Science.

## Contents of the repository
- The thesis in PDF format: [Architectures_of_Leading_Image_Captioning_Systems.pdf](Architectures_of_Leading_Image_Captioning_Systems.pdf) (46 MB)
- [CocoResults](/CocoResults): The Microsoft COCO Image Captioning Challenge results at 31.3.2021 as a CSV file
- [Images](Images/): has just one image (equal to figure 5.2 in the thesis) to give an example of the image captioning task.
- [Indesign](/Indesign): the Adobe InDesign files (.indd) for the original images in the thesis (architecture images, computer vision & NLG task map, 3-phase training). The folder also contains three intermediate images (.png) used in the 3-phase training image.
- [Latex](/Latex): the Latex source files for the thesis, exluding the images cited from previous works (these are excluded to be on the safe side regarding copyrights. The subfolder [Latex/images-indesign](/Latex/images-indesign) has the original images (architecture images, computer vision & NLG task map, 3-phase training) in .png format.

## Image captioning as a machine learning task
![Example image with object segmentations and captions](/Images/Figure_5_2_Sample_image_and_captions.png)
*An example of an image, object segmentations and five ground truth captions* (figure 5.2. in the thesis). *Left*: a sample COCO image. *Center*: ground-truth pixel-level segmentations of foreground objects for the same image. *Right*: the five ground truth captions for the image. Image and caption source: COCO, https://cocodataset.org/#explore?id=51052.

![Image captioning in the fields of computer vision and natural language generation](/Latex/images-indesign/Task_map.png)
Image captioning as a machine learning task uses techniques from two fields of research: computer vision and natural language generation.

## Abstract of the thesis
**Image captioning** is the task of generating a natural language description of an image. The task requires techniques from two research areas, computer vision and natural language generation.

This thesis investigates the architectures of leading image captioning systems. The **research question** is: *What components and architectures are used in state-of-the-art image captioning systems and how could image captioning systems be further improved by utilizing improved components and architectures?* Five openly reported leading image captioning systems are investigated in detail: Attention on Attention, the Meshed-Memory Transformer, the X-Linear Attention Network, the Show, Edit and Tell method, and Prophet Attention.

The investigated leading image captioners all rely on the same object detector, the Faster R-CNN based Bottom-Up object detection network. Four out of five also rely on the same backbone convolutional neural network, ResNet-101. Both the backbone and the object detector could be improved by using newer approaches. Best choice in CNN-based object detectors is the EfficientDet with an EfficientNet backbone. A completely transformer-based approach with a Vision Transformer backbone and a Detection Transformer object detector is a fast-developing alternative. The main area of variation between the leading image captioners is in the types of attention blocks used in the high-level image encoder, the type of natural language decoder and the connections between these components. The best architectures and attention approaches to implement these components are currently the Meshed-Memory Transformer and the bilinear pooling approach of the X-Linear Attention Network. Implementing the Prophet Attention approach of using the future words available in the supervised training phase to guide the decoder attention further improves performance.

Pretraining the backbone using large image datasets is essential to reach semantically correct object detections and object features. The feature richness and dense annotation of data is equally important in training the object detector.

## Architecture images
<details>
  <summary>Architecture images of 5 leading captioning systems</summary><details>
    <img src="/Latex/images-indesign/Architecture_AoA.png" name="Attention on Attention"/>
    <img src="/Latex/images-indesign/Architecture_M2.png" name="Meshed-Memory Transformer"/>
    <img src="/Latex/images-indesign/Architecture_X-LAN.png" name="X-Linear Network"/>
    <img src="/Latex/images-indesign/Architecture_ShowEdit.png" name="Show, Edit and Tell"/>
    <img src="/Latex/images-indesign/Architecture_Prophet.png" name="Prophet Attention"/>
</details>


## Links
### COCO online test server results
- [Microsoft COCO Image Captioning Challenge online test server results](https://competitions.codalab.org/competitions/3221#results)

### Selected datasets
- [COCO](https://cocodataset.org/#home)
- [COCO-Stuff](https://github.com/nightrome/cocostuff)
- [Visual Genome](https://visualgenome.org/)
- [ImageNet](https://www.image-net.org/) 
- [Personality-Captions](https://parl.ai/projects/personality_captions/)
- [Localized Narratives](https://google.github.io/localized-narratives/)

### Toolkits
- [Detectron2](https://github.com/facebookresearch/detectron2)

## Note on using images
The original images by Mikko Kotola (described above) may be used and modified under the [MIT license](LICENSE). The permissions to use images cited from elsewhere should be checked from the original sources, which are referenced in the thesis.