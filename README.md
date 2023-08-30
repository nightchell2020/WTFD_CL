# WTFD_CL : Integrated Fault Diagnostic Model of High Speed and Low Speed Bearing of Large Wind Power Generators using Continual Learning

### Injae Lee


## About Code
Collaborative Research of Doosan&CAU

You have to modify `config.py`to select mode as Auto-Encoder or WDCNN
### 1. Environment setup
This code has been tested on 
- Window10 Python 3.8.3, Pytorch 1.7.1 (main)
- Ubuntu 20.04, Python 3.8.3, Pytorch 0.7.0/1.6.0, CUDA 10.2.

Please install related libraries before running this code: 
```bash
pip install -r requirements.txt
```
**Note** Also check your data-path in `config.py` 

### 2. Test & Evaluation
Download pretrained model: [general_model](https://pan.baidu.com/s/1QeU7OcTqHksZXscBq3skiw)(code: c99t) and put it into `tools/snapshot` directory.

Download testing datasets and put them into `test_dataset` directory. If you want to test the tracker on a new dataset, please refer to [pysot-toolkit](https://github.com/StrangerZhang/pysot-toolkit) to set test_dataset.

```bash 
python test.py                                
	--dataset A                 #dataset_name
	--snapshot snapshot/general_model.pth  # tracker_name
```
The testing result will be saved in the `results/dataset_name/tracker_name` directory.

### 3. Train

#### Prepare training datasets

Used datasets：
* [A]
* [B]
* [C]

#### Train a model
To train the SiamAD model, run `train.py` with the desired configs:

```bash
cd tools
python train.py
```

### 4. Contact
If you have any questions, please contact me.

IPIS

Injae Lee

Email: [injea0908@ipis.cau.ac.kr](injea0908@ipis.cau.ac.kr)


## Acknowledgement
The code is implemented based on [pysot](https://github.com/STVIR/pysot). We would like to express our sincere thanks to the contributors.