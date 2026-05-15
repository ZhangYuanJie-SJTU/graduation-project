# 毕业设计 — 面向心律失常老人的可穿戴多体征监护系统

> **Graduation Project — Wearable Multi-Sign Monitoring System for Elderly with Arrhythmia**
> *基于 ESP32-S3 + FPC 柔性电路 + TFLite 边缘 AI + OneNET 云平台 + 微信小程序的全链路健康监护解决方案*

[![University](https://img.shields.io/badge/University-武汉理工大学-blue)](https://www.whut.edu.cn/)
[![Degree](https://img.shields.io/badge/Degree-本科毕业设计-purple)]()
[![Tech](https://img.shields.io/badge/Tech-ESP32--S3%20%2B%20TFLite-brightgreen)]()
[![Cloud](https://img.shields.io/badge/Cloud-OneNET-blue)]()
[![Platform](https://img.shields.io/badge/Platform-WeChat%20Mini%20Program-green)]()

---

## 项目概览

| 项目 | 内容 |
|------|------|
| **课题** | 面向心律失常老人的可穿戴多体征监护系统设计 |
| **作者** | 张元杰 |
| **院校** | 武汉理工大学 |
| **指导老师** | 刘老师 |
| **日期** | 2026 年 4 月 |

---

## 核心能力

| 模块 | 技术方案 | 说明 |
|------|---------|------|
| **主控** | ESP32-S3 | 双核 Xtensa LX7, Wi-Fi + BLE 5.0 |
| **传感前端** | FPC 柔性电路 | 心电(ECG)、血氧(SpO2)、体温、体动 |
| **边缘 AI** | TensorFlow Lite Micro | 心律失常实时分类推理 |
| **云平台** | OneNET | 数据上传、存储、远程监控 |
| **用户端** | 微信小程序 | 实时数据显示、异常报警、历史趋势 |

---

## 系统架构

```
┌─────────────────────────────────────────────────────────┐
│                    可穿戴终端层                           │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐              │
│  │ ECG 电极 │  │ SpO2 传感器│  │ 温度/加速度│              │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘              │
│       └──────────┬──┴─────────────┘                     │
│            ┌─────▼─────┐                                │
│            │  ESP32-S3  │ ← TFLite Micro 推理            │
│            └─────┬─────┘                                │
└──────────────────┼──────────────────────────────────────┘
                   │ Wi-Fi
┌──────────────────▼──────────────────────────────────────┐
│                    云端服务层                             │
│            ┌─────────────┐                              │
│            │   OneNET    │ 数据存储 + 告警推送            │
│            └──────┬──────┘                              │
└───────────────────┼─────────────────────────────────────┘
                    │ API
┌───────────────────▼─────────────────────────────────────┐
│                    用户交互层                             │
│            ┌─────────────┐                              │
│            │ 微信小程序   │ 实时监控 + 历史趋势           │
│            └─────────────┘                              │
└─────────────────────────────────────────────────────────┘
```

---

## 快速开始

### 在线查看

| 文件 | 说明 | 链接 |
|---|---|---|
| 介绍解读-final.html | 项目介绍与解读（最终版） | [在线预览](https://zhangyuanjie-sjtu.github.io/graduation-project/final/介绍解读-final.html) |
| 技术展示-final.html | 技术方案展示（最终版） | [在线预览](https://zhangyuanjie-sjtu.github.io/graduation-project/final/技术展示-final.html) |
| 答辩PPT-final.html | 答辩 PPT（最终版） | [在线预览](https://zhangyuanjie-sjtu.github.io/graduation-project/final/答辩PPT-final.html) |
| 答辩稿.md | 答辩演讲稿（Markdown） | [查看](https://zhangyuanjie-sjtu.github.io/graduation-project/final/答辩稿.md) |
| 答辩稿.docx | 答辩演讲稿（Word） | [下载](https://github.com/ZhangYuanJie-SJTU/graduation-project/raw/main/final/答辩稿.docx) |

### 历史版本

| 版本 | 页面标题 | 链接 |
|---|---|---|
| v1.0 | 面向心律失常老人的可穿戴多体征监护系统 | [查看](https://zhangyuanjie-sjtu.github.io/graduation-project/v1/) |
| v2.0 | 面向心律失常老人的可穿戴多体征监护系统 | [查看](https://zhangyuanjie-sjtu.github.io/graduation-project/v2/) |
| v3.0 | 可穿戴多体征监护系统 — 毕业设计答辩 | [查看](https://zhangyuanjie-sjtu.github.io/graduation-project/v3/) |
| v4.0 | 可穿戴多体征监护系统 — 毕业设计答辩 | [查看](https://zhangyuanjie-sjtu.github.io/graduation-project/v4/) |
| v4.1 | 可穿戴多体征监护系统 — 毕业设计答辩 | [查看](https://zhangyuanjie-sjtu.github.io/graduation-project/v4.1/) |
| v5.0 | 可穿戴多体征监护系统 — 毕业设计答辩 | [查看](https://zhangyuanjie-sjtu.github.io/graduation-project/v5/) |

---

## 仓库结构

```
graduation-project/
├── index.html              # 导航首页
├── final/                  # 最终版本文件
│   ├── 介绍解读-final.html # 项目介绍与解读
│   ├── 技术展示-final.html # 技术方案展示
│   ├── 答辩PPT-final.html  # 答辩 PPT
│   ├── 答辩稿.md           # 答辩演讲稿 (Markdown)
│   └── 答辩稿.docx         # 答辩演讲稿 (Word)
├── v1/ ~ v5/               # 历史版本展示页面
└── README.md
```

---

## 作者

| | 姓名 | 单位 | 联系方式 |
|---|---|---|---|
| **作者** | 张元杰 | 武汉理工大学 → 上海交通大学（保研推免） | [GitHub](https://github.com/ZhangYuanJie-SJTU) |

---

## 许可证

本仓库存储本科毕业设计相关材料，版权归作者所有。
