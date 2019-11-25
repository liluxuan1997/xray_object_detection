
# Installation 
This object detection repo implementation is based on [mmdetection](https://github.com/open-mmlab/mmdetection). Therefore the installation is the same as original mmdetection.

Please check [INSTALL.md](INSTALL.md) for installation instructions.


## Train and inference
The configs are in [configs/](configs/).

### Inference
    # single-gpu testing
    python tools/test.py ${CONFIG_FILE} ${CHECKPOINT_FILE} [--out ${RESULT_FILE}] --eval bbox [--show]
    
    # multi-gpu testing
    ./tools/dist_test.sh ${CONFIG_FILE} ${CHECKPOINT_FILE} ${GPU_NUM} [--out ${RESULT_FILE}] --eval bbox

### Training
    # single-gpu training
    python tools/train.py ${CONFIG_FILE}
    
    # multi-gpu training
    ./tools/dist_train.sh ${CONFIG_FILE} ${GPU_NUM} [optional arguments]
    
## Dataset
Since the dataset of our project follows the format of VOC dataset. The orignization should be

    +--data

         +--VOCdeckit
   
              +--VOC2007
       
                   +--Annotations
           
                   +--ImageSets
           
                   +--JpegImages

## Models

### Faster-RCNN

### FoveaBox

### Cascade-RCNN
Please check [GETTING_STARTED.md](GETTING_STARTED.md) for detailed instructions.