---
title: Python 安装指南
date: 2022-04-21 19:24:15
categories:
tags: 编程
---

# Python 安装指南
使用 Anaconda  和 jupyter 笔记本写 Python

## 安装 Anaconda 
- 下载并安装
https://www.anaconda.com/products/individual#Downloads

- conda 官方文档
https://docs.conda.io/projects/conda/en/latest/user-guide/index.html


### Windows 下激活虚拟环境需要初始化
刚安装完 Anaconda，在 windows powershell 中是无法激活虚拟环境的。为了开启激活，需要在终端里执行：
```
conda init powershell
```

- 在 Terminal 里查看使设置成功
```python
conda --version
python --version
```

## 打开 Jupyter
```python
# 打开 jupyter notebook
jupyter notebook
# 打开 jupyter lab

# conda install -c conda-forge jupyterlab
jupyter lab
```

## 用 conda 创建 python 虚拟环境
1. 查看当前存在哪些虚拟环境
```python
conda env list
# 或者 conda info -e
```
2. Python 创建虚拟环境
```python
conda create -n your_env_name python=x.x
```
3. 激活或者关闭虚拟环境
```shell
conda activate env_name
conda deactivate
# 切换到 root 环境
conda activate root
```
4. 删除虚拟环境
```bash
conda remove -n env_name --all
```
