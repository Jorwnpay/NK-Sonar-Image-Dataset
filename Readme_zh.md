# NK-Sonar-Image-Dataset (NKSID)

[Eng](https://github.com/Jorwnpay/NK-Sonar-Image-Dataset/blob/main/Readme.md)|简体中文

这个仓库发布了一个全新的前视声纳图像识别基准测试，名为NanKai Sonar Image Dataset（NKSID）。该数据集包含来自8个类别的2617张图片，标签呈现自然的长尾分布。

### 介绍

我们在渤海湾（ $39^\circ N 118^\circ E$ ）采集了数据，如图1(a)左侧所示。具体来说，我们使用一台配备多波束前视声纳（Oculus M750d）的遥操作潜水器（ROV）来获取水下数据。为了减少目标之间的干扰并便于定位，我们使用绳索将目标固定在浮标上，悬挂在水面下约5-10米的深度。如图1(a)右侧所示，按照固定间隔放置目标。在数据采集过程中，我们从不同角度、量程（2-15米）和频率（750kHz、1.2MHz）获取了每个目标的图像，以增强数据集的丰富性。随后，对目标进行了筛选、预处理和标注，最终形成了包含8个类别的2617张图像。图1(b)展示了每个类别的光学和声纳图像示例，NKSID呈现自然长尾分布。

<img src=".\img\data_info.png" style="zoom:60%;" />

### 使用方法

直接从该仓库下载数据集，解压文件夹下的全部`.zip`压缩包。由于单个文件超过Github上传上限，我们将每个类别的图片都分别压缩，其中tire文件夹中包含两个压缩包，需要分别解压。 `train_abs.txt`保存了每张图片的相对路径和标签。 `kfold_train.txt`和`kfold_val.txt`保存了十次五折交叉验证的随机“训练集/验证集”划分方案，里面的数字$n$代表样本序号，对应样本在`train_abs.txt`中的第$n$行。 使用Demo：一个使用该数据集进行开放集长尾识别的仓库：[Jorwnpay/Sonar-OLTR (github.com)](https://github.com/Jorwnpay/Sonar-OLTR).

### Citation

本数据集涉及到的论文正在接受审查，如果该数据集对您有用，请考虑引用我们：

```latex
TODO...
```

