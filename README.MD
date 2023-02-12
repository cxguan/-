# 深度学习课程设计——代码运行步骤
小组成员：

智科（3） 欧阳清华

智科（2） 官晨芯 

## 1、导入数据集 
把数据集下载并解压在```./datasets```文件夹下

## 2、数据集地址归纳
修改并运行`./datasets`文件夹下的`data_process.py`文件,以```./datasets/image_train/T1.3BPFFJdXXXXXXXX_!!0-item_pic.jpg.jpg	./datasets/txt_train/T1.3BPFFJdXXXXXXXX_!!0-item_pic.jpg.txt```
的格式归纳每个训练集和验证集的图片与标签对应路径，分别保存在`train.txt`和`test.txt`中

## 3、修改训练参数
在
```
./config/icdar2015_resnet18_FPN_DBhead_polyLR.yaml
```
中修改数据集地址、训练轮次、`batch_size`等参数

## 4、训练模型 
运行指令
```
python (train.py文件地址) --config_file "(icdar2015_resnet18_FPN_DBhead_polyLR.yaml文件地址)"
```
训练模型

## 5、生成结果
运行指令
```
python (predict.py文件地址) --model_path （模型地址) --input_folder （待处理图片地址) --output_folder （结果文件地址)"
```
识别图片并生成结果
