# 胸腹部CT多器官智能量化分析系统

**基于 TotalSegmentator 的呼吸-消化系统疾病赛道量化分析项目**

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-ee4c2c.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 项目简介

本项目针对**“呼吸-消化系统疾病”赛道**的**影像量化分析题**，构建了一个端到端的胸腹部CT智能量化分析系统。

使用 TotalSegmentator 进行多器官分割，重点实现多个临床关键指标的**自动量化计算**，并生成标准化报告。项目强调 **Baseline vs Proposed** 对比实验，突出算法的先进性和临床实用性。

### 核心指标
- 肺体积 + 肺气肿指数（低衰减区占比）
- 肝脏脂肪浸润量化（平均HU值）
- 胰腺实质萎缩率
- 气道锥度 + 弯曲度（**核心创新指标**）
- 肺结节体积 + 毛刺指数

---

## 安装与使用

### 1. 环境安装

```bash
conda create -n ts python=3.11
conda activate ts

pip install -r requirements.txt
```
### 2. 项目结构
chest-abdomen-ct-quantification/
```
├── src/                  # 核心代码
│   ├── segment.py        # TS分割模块
│   ├── quantify.py       # 量化计算
│   ├── main.py           # 主流程入口
│   └── utils.py
├── data/                 # 数据集
├── output/               # 分割结果
├── results/              # 实验结果
├── reports/              # 生成的PDF报告
├── config/               # 配置文件
└── README.md
```
## 数据集

TotalSegmentator Dataset：多器官分割测试

AMOS：腹部器官（肝、胰腺）微调与验证

ATM’22：气道树精细标注（气道参数）

LIDC-IDRI：肺结节量化

所有数据集均为公开数据集，已在报告中注明来源。
