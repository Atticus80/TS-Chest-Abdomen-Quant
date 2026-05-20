# 胸腹部CT多器官智能量化分析系统

**基于 TotalSegmentator 的呼吸-消化系统疾病赛道量化分析项目**

[![Python](https://img.shields.io/badge/Python-3.11-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-ee4c2c.svg)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📋 项目简介

本项目针对**“呼吸-消化系统疾病”赛道**的**影像量化分析题**，构建了一个端到端的胸腹部CT智能量化分析系统。

使用 TotalSegmentator 进行多器官分割，重点实现多个临床关键指标的**自动量化计算**，并生成标准化报告。项目强调 **Baseline vs Proposed** 对比实验，突出算法的先进性和临床实用性。

### 核心指标
- **肺体积** + **肺气肿指数**（低衰减区占比）
- **肝脏脂肪浸润量化**（平均HU值）
- **胰腺实质萎缩率**
- **气道锥度 + 弯曲度**（核心创新指标）
- **肺结节体积 + 毛刺指数**

---

## 🛠️ 安装与使用

### 1. 环境安装

```bash
conda create -n ts python=3.11
conda activate ts

pip install -r requirements.txt
