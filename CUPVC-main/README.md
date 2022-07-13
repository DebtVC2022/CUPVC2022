# CUPVC-for-optimizing-telephone-banking-service

CUPVC is an unsupervised voice conversion framework designed to improve telephone banking service performance. On the basis of fully learning the prosody information of the operators, it converts the prosody of the poorly-performing operators into the prosody of the good well-performing operators, thereby realizing the improvement of the service performance of the poorly-performing operators.

## Methodology

Flowchart of CUPVC

- Training phase

![image](https://github.com/WSYcurry/DebtVC/blob/main/DebtVC2022/DebtVC_Overview_training.bmp)

- Conversion phase

![image](https://github.com/WSYcurry/DebtVC/blob/main/DebtVC2022/DebtVC_Overview_conversion.bmp)

Design motivation of CUPVC forge module

![image](https://github.com/WSYcurry/DebtVC/blob/main/DebtVC2022/forge_function_with_arrow.bmp)

If you find this work useful and use it in your research, please consider citing our paper.

## Audio demos

We show some audio demos, and if you want to obtain the large-scale dataset of telephone recordings in the practical scenarios of telephone banking service, please contact us.

## Dependencies

- Python 3.8
- multiprocessing
- queue
- Numpy
- math
- Scipy
- PyTorch >= v1.2.0
- librosa
- pysptk
- soundfile
- matplotlib
- wavenet_vocoder pip install wavenet_vocoder==0.1.1 for more information, please refer to https://github.com/r9y9/wavenet_vocoder


## To training

The training process of CUPVC consists of two parts, the first is to train the timbre constraint, the prosody constraint and the nonoverlapping information constraint, and then further train the reconstruction loss of mel.

Please use the scripts to prepare your own data for training.

- Extract spectrogram and f0(Training phase): python data_loader.py

- Run the training scripts(Training phase): python train.py

- Run the forge scripts(Conversion phase): python forge_demo.py
