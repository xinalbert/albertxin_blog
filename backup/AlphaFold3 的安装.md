## 首先第一步是申请权重文件
[权重文件](https://docs.google.com/forms/d/e/1FAIpQLSfWZAgo1aYk0O4MuAXZj8xRQ8DafeFJnldNOnh_13qAx2ceZw/viewform?pli=1)如果有国外大学的邮箱可能会好申请一点。
## 安装
### 准备代码数据
- 下载代码
```shell
git clone https://github.com/google-deepmind/alphafold3.git
```
我一般直接从GitHub下载zip的格式，然后解压
- 进入AlphaFold3文件夹，并下载数据
```shell
cd alphafold3 && mkdir database
nohup bash ./fetch_databases.sh database >download.log 2>&1 &
```
下载完后我们就可以安装了
### 创建新的环境
- 环境创建
```shell
conda create -n alphafold3
conda activate -n alphafold3
```
- 安装hmmer，和Python
```shell
conda install bioconda::hmmer
conda install python=3.11
```
- 安装依赖
```shell
conda install cmake
conda install nvidia::cuda-cudart
pip install -r dev-requirements.txt
conda install conda-forge::abseil-cpp
conda install conda-forge::pybind11-abi
conda install conda-forge::pybind11
conda install conda-forge::catch2
conda install bioconda::libcifpp
conda install salilab::dssp
conda install conda-forge::libzlib
conda install conda-forge::icu
conda install zlib
```
- 安装AlphaFold3
```shell
pip install .

```
- 建立数据库
```shell
build_data
```
如果没有问题的话，应该就安装好了，就可以使用了。

#### 参考了这篇专栏：[通过conda安装AlphaFold3](https://zhuanlan.zhihu.com/p/10998885375)

如果觉得有帮助，欢迎请我喝杯咖啡！
paypal：PayPal.Me/abertxin

Gmeek-html<img src="https://xinalbert.github.io/albertxin_blog/coffee/ali.jpeg" alt="Image 1" style="width:30%; margin-right:5%;" /> Gmeek-html<img src="https://xinalbert.github.io/albertxin_blog/coffee/wecaht.jpeg" alt="Image 2" style="width:30%;" />