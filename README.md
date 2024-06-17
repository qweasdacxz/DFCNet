# DFCNET
This repo holds codes of the paper: DFCNet: Cross-Modal Dynamic Feature Contrast Net for Continuous Sign Language Recognition.

This repo is based on [CorrNet](https://github.com/hulianyuyy/CorrNet) & [TLP](https://github.com/hulianyuyy/Temporal-Lift-Pooling). Many thanks for those great work!

## Installation
-This project is implemented in Pytorch(1.13.0). Thus please install Pytorch first.

- You can install other required modules by conducting 
   `pip install -r requirements.txt`
## Data Preparation
We read and process the same way as [CorrNet](https://github.com/hulianyuyy/CorrNet).

## Inference

### PHOENIX2014 dataset

| Backbone | Dev WER  | Test WER  | Pretrained model                                             |
| -------- | ---------- | ----------- | --- |
| ResNet34 | 17.6%      | 18.3%       | [[Baidu]](https://pan.baidu.com/s/1111) (passwd: 1111)<br />[[Google Drive]](https://drive.google.com/file/11111) |



### PHOENIX2014-T dataset

| Backbone | Dev WER  | Test WER  | Pretrained model                                             |
| -------- | ---------- | ----------- | --- |
| ResNet34 | XXX%      | XXX%       | On the way |

### CSL-Daily dataset

To evaluate on CSL-Daily with this checkpoint, you need to replace the resnet.py code with the code from resnet1.py.

| Backbone | Dev WER  | Test WER  | Pretrained model                                            |
| -------- | ---------- | ----------- | --- |
| ResNet34 | 26.4%      | 26.5%       | On the way |


To evaluate the pretrained model, start by selecting the dataset in line 3 of ./config/baseline.yaml, and then execute the following command: 
`python main.py  --load-weights path_to_weight.pt --phase test`

<!-- 
### Citation

If you find this repo useful in your research works, please consider citing: -->
