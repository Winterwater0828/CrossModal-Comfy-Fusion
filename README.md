# CrossModal-Comfy-Fusion

## 📖 项目简介

本项目主要研究基于大语言模型和视觉生成模型的图像任务自动化编辑与风格转换。通过深度学习技术，系统能够根据用户的文本指令，自动进行图像合成、风格迁移和细节增强等操作，实现个性化定制。同时探索图像编辑的多模态融合，支持从图像内容理解到风格转换的全链路处理。

## 🎯 项目目标

1. **AIGC 技术调研**：深入调研当前 AIGC 领域的主流技术，包括文生图、图生图、视频生成等方向的最新进展
2. **ComfyUI 实验验证**：基于 ComfyUI 搭建 Flux.2 工作流，进行实际图像生成实验，验证技术可行性

## 🏗️ 项目结构

```
CrossModal-Comfy-Fusion/
├── 📊 调研文档/
│   ├── Color Grading调研.pdf          # 色彩校正技术调研
│   ├── Video调研.pdf                  # 视频生成技术调研
│   ├── 调研编辑生成PSD格式.pdf        # PSD格式编辑生成调研
│   └── 大模型图像编辑项目.py.pdf      # 大模型图像编辑项目方案
├── 🔧 ComfyUI 工作流/
│   ├── 文生图.json                    # 文生图工作流配置
│   └── image_flux2_klein_text_to_image.json  # Flux.2 文生图工作流
├── 🖼️ 生成图像样例/
│   ├── Flux2-Klein_00001_.png        # Flux.2 生成图像样例1
│   ├── Flux2-Klein_00002_.png        # Flux.2 生成图像样例2
│   ├── Flux2-Klein_00003_.png        # Flux.2 生成图像样例3
│   └── 猫爬架.jpg                     # 测试图像
├── 📝 教程文档/
│   └── 教程_搭建Flux2工作流 → 对接runninghub训练...  # Flux2 工作流搭建教程
└── 🛠️ ComfyUI 核心（基于官方源码）
```

## 🚀 快速开始

### 环境要求

- Python 3.10+
- CUDA 11.8+（推荐使用 NVIDIA GPU）
- ComfyUI 最新版本

### 安装步骤

1. **安装 ComfyUI**
```bash
git clone https://github.com/comfyanonymous/ComfyUI.git
cd ComfyUI
pip install -r requirements.txt
```

2. **使用本项目工作流**
   - 将 `文生图.json` 或 `image_flux2_klein_text_to_image.json` 拖入 ComfyUI
   - 确保已下载对应的模型文件
   - 点击 "Queue Prompt" 运行工作流

### Flux.2 工作流说明

`image_flux2_klein_text_to_image.json` 是基于 Flux.2 模型的文生图工作流，支持：
- 高质量文本到图像生成
- 精细化的参数控制
- 可自定义提示词和生成参数

## 📚 调研内容

### AIGC 技术方向
- **文生图技术**：Stable Diffusion、DALL-E、Midjourney、Flux 等主流模型对比
- **图生图技术**：图像编辑、风格迁移、图像修复等技术
- **视频生成**：Sora、Runway Gen、Pika 等视频生成模型调研

### 重点研究
- Flux.2 模型在图像生成中的应用
- 多模态融合的图像编辑方案
- 自动化图像处理流程设计

## 🎨 实验结果展示

以下是使用 Flux.2 工作流生成的图像样例：

| 样例1 | 样例2 |
|:---:|:---:|
| ![样例1](Flux2-Klein_00001_.png) | ![样例2](Flux2-Klein_00002_.png) |

## 🎨 物体替换对比展示

| 原图-猫爬架 | 生成-狗狗 |
|:---:|:---:|
| ![原图-猫爬架](猫爬架.jpg) | ![生成-狗狗](Flux2-Klein_00003_.png) |

## 📝 使用说明

### 导入工作流
1. 打开 ComfyUI 界面
2. 点击 "Load" 按钮
3. 选择 `.json` 工作流文件
4. 根据需要调整提示词和参数

### 自定义修改
- 可替换提示词生成不同风格图像
- 调整采样步数和 CFG Scale 控制生成质量
- 修改图像尺寸以适应不同需求

## 📄 许可证

本项目采用 GPL-3.0 许可证 - 详见 [LICENSE](LICENSE) 文件

## 📧 联系方式

如有问题或建议，欢迎通过 GitHub Issues 进行交流

## 🙏 致谢

- [ComfyUI](https://github.com/comfyanonymous/ComfyUI) - 强大的节点式 UI 框架
- [Flux](https://github.com/black-forest-labs/flux) - 先进的图像生成模型

---

**⭐ 如果这个项目对你有帮助，欢迎点赞收藏！**

