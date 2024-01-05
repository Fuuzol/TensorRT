# TensorRT
TensorRT部署

1、下载前相关查询：
查看显卡驱动版本：nvidia-smi
查看cuda版本：nvcc -V
cuda与显卡驱动对应表：https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html#title-new-features

2、下载链接：
https://developer.nvidia.com/nvidia-tensorrt-8x-download

3、安装
将下载好的软件包，上传至Linux操作系统任意用户目录下
解压：tar -zxvf TensorRT-8.6.1.6.Linux.x86_64-gnu.cuda-11.8.tar.gz

拷贝至指定安装目录。将解压得到的TensorRT-8.0.1.6目录拷贝至/opt目录下：
sudo cp -R TensorRT-8.6.1.6 /opt

设置环境变量。打开/etc/profie文件，添加TensorRT库的搜索路径：
sudo vi /etc/profile

添加：export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/opt/TensorRT-8.6.1.6/lib

使环境变量生效。
source /etc/profile

4、测试TensorRT安装
进入到TensorRT安装目录下的手写数字识别samples，执行编译，执行测试：
cd /opt/TensorRT-8.6.1.6/samples/sampleOnnxMNIST
sudo make
../../bin/sample_onnx_mnist
