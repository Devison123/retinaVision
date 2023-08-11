

**Step 1**: Produce txt results and visualizations from model.
```bash
# Test ResNet50 backbone model
python test_widerface.py --cfg_path="./configs/retinaface_res50.yaml" --gpu=0
# or
# Test ResNet50 backbone model
python test_widerface.py --cfg_path="./configs/retinaface_mbv2.yaml" --gpu=0
```

Note:
- The visualizations results would be saved into `./results/`.


```

### Detect on Input Image

You can detect on your image by the model. For example, detect on the image from [./data/0_Parade_marchingband_1_149.jpg](https://github.com/peteryuX/retinaface-tf2/blob/master/data/0_Parade_marchingband_1_149.jpg) as following.

```bash
python test.py --cfg_path="./configs/retinaface_res50.yaml" --img_path="./data/0_Parade_marchingband_1_149.jpg" --down_scale_factor=1.0

```

Note:
- You can down scale your input by the `--down_scale_factor`.

### Demo on Webcam

Demo face detection on your webcam.
```bash
python test.py --cfg_path="./configs/retinaface_res50.yaml" --webcam=True --down_scale_factor=1.0
# or





## References
:hamburger:

Thanks for these source codes porviding me with knowledges to complete this repository.

- https://github.com/deepinsight/insightface/tree/master/detection/retinaface (Official)
    - Face Analysis Project on MXNet http://insightface.ai
- https://github.com/biubug6/Pytorch_Retinaface
    - Retinaface get 80.99% in widerface hard val using mobilenet0.25.
- https://github.com/wondervictor/WiderFace-Evaluation
    - Python Evaluation Code for Wider Face Dataset
- https://github.com/zzh8829/yolov3-tf2
    - YoloV3 Implemented in TensorFlow 2.0
