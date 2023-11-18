# Submission10296
The lmplementation for submission 10296

## Requirements

- python 3.9
- pytorch 2.0.1
- torchvision 0.15.2

## Data Preparation

The datasets are provided in the anonymous [link](https://drive.google.com/drive/folders/1x36Dpv7FMSxx6LtVmwiFkyhKhTG3u1bI?usp=sharing).

```
dataset
├── BUSI
│   ├── test
│   	├── images
│   	├── masks
│   ├── train
│   	├── images
│   	├── masks
├── DSB
│   ├── test
│   ├── train
├── Polyp
│   ├── test
│   	├── CVC-ClinicDB
│   	├── CVC-ColonDB
│   	├── ETIS-LaribPolypDB
│   	├── Kvasir
│   	├── test
│   ├── train
```

### Pretrained Backbone

The pretrained backbone is provided in the anonymous [link](https://drive.google.com/file/d/1QtMs4uSyXVHS9uYZAj4_HDzfBAlG6UJG/view?usp=sharing), and place it into `./pretrained_pth`.

```
pretrained_pth
├── pvt_v2_b2.pth
```

## Training

Run the command scripts in `run/` to train models on different datasets. For example,  to train a breast ultrasound image segmentation model, run:

```
sh run/train_busi.sh
```

## Evaluating

The trained model are provided in the following anonymous links ([DSNet_BUSI](https://drive.google.com/file/d/1XFV-D0AfsiaWkx-9Q8kS9wTIX6rleY55/view?usp=sharing), [DSNet_DSB](https://drive.google.com/file/d/1i0rskLdInlGuR0slUO8DTCq2ITIcwuVw/view?usp=sharing), [DSNet_Polyp](https://drive.google.com/file/d/1Ove07h2nCHv6L0UFRboEbyjgiAf7jvD-/view?usp=sharing)). To evaluate them, download the model file and place it into `./model` and then run the command script in `run/`. For example,  to evaluate a breast ultrasound image segmentation model, run:

```
sh run/test_busi.sh
```


