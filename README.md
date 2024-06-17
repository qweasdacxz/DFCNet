# DFCNET_CSLR
This repo holds codes of the paper: DFCNet: Cross-Modal Dynamic Feature Contrast Net for Continuous Sign Language Recognition.

This repo is based on [CorrNet](https://github.com/hulianyuyy/CorrNet)[TLP](https://github.com/hulianyuyy/Temporal-Lift-Pooling). Many thanks for their great work!

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
| ResNet34 | 17.6%      | 18.3%       | [[Baidu]](https://pan.baidu.com/s/1DIGts18fdh4Fdw_y7ZQ6XA) (passwd: skd3)<br />[[Google Drive]](https://drive.google.com/file/d/1Xt_4N-HjEGlVyrMENydsxNtpVMSg5zDb/view?usp=share_link) |



### PHOENIX2014-T dataset

| Backbone | Dev WER  | Test WER  | Pretrained model                                             |
| -------- | ---------- | ----------- | --- |
| ResNet18 | 18.9%      | 20.5%       | [[Baidu]](https://pan.baidu.com/s/1osUDzpPhKPDavxyvqOrVfQ) (passwd: deuq)<br />[[Google Drive]](https://drive.google.com/file/d/1c_wNHYMqCbqRE5KqrQL1P6chOw5VBS6Q/view?usp=share_link) |

### CSL-Daily dataset

To evaluate on CSL-Daily with this checkpoint, you need to replace the resnet.py code with the code from resnet1.py.

| Backbone | Dev WER  | Test WER  | Pretrained model                                            |
| -------- | ---------- | ----------- | --- |
| ResNet18 | 30.6%      | 30.1%       | [[Baidu]](https://pan.baidu.com/s/1WzNltivGRbfV33wkM4rzjg) (passwd: u2iv)<br />[[Google Drive]](https://drive.google.com/file/d/1-aSKPe9cVkvHeiJuyQm3HlZ5u63CI-mm/view?usp=share_link) |


To evaluate the pretrained model, start by selecting the dataset in line 3 of ./config/baseline.yaml, and then execute the following command: 
`python main.py  --load-weights path_to_weight.pt --phase test`


### Citation

If you find this repo useful in your research works, please consider citing:
