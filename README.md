# GLASS

无监督方法用于检测各种缺陷，如划痕、破碎、脏污、裂痕等


## 依赖
环境配置
```
conda create -n glass_env python=3.9.15
conda activate glass_env
pip install -r requirements.txt
```

## 数据集地址
- DTD ([Download link](https://www.robots.ox.ac.uk/~vgg/data/dtd/))
- MVTec AD ([Download link](https://www.mvtec.com/company/research/datasets/mvtec-ad/))
- VisA ([Download link](https://github.com/amazon-science/spot-diff/))
- MPDD ([Download link](https://github.com/stepanje/MPDD/))

## 训练
DTD为辅助生成异常的数据集，必须下载，然后训练自己的数据集可按照MPDD数据集构建方式，使用good文件夹下训练，缺陷作为验证。

Edit `./shell/run-dataset.sh` to configure arguments `--datapath`, `--augpath`, `--classes`, and hyperparameter settings.
Please modify argument `--test` to 'ckpt' / 'test' to toggle between training and testing modes.

```
bash run-mpdd.sh 
```



