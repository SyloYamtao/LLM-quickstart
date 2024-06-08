# 1 安装环境
## 更新apt-get库
apt-get update apt-get 
## 安装必要软件
install git-lfs curl aria2
# 2 安装脚本并配置环境变量
wget https://hf-mirror.com/hfd/hfd.sh
chmod a+x hfd.sh 
export HF_ENDPOINT=https://hf-mirror.com
echo 'export HF_ENDPOINT=https://hf-mirror.com' >> ~/.bashrc && source ~/.bashrc
# 3 设置别名
echo 'export PATH="$PATH:$PWD"' >> ~/.bashrc && echo 'alias hfd="$PWD/hfd.sh"' >> ~/.bashrc && source ~/.bashrc
# 4 下载模型数据
## 下载模型数据
hfd 模型名 --tool aria2c -x 4 
## 下载数据集数据
hfd 数据名 --dataset --tool aria2c -x 4