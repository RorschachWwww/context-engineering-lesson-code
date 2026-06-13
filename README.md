# Context Engineering Notebooks

这个代码库用于存放微信公众号“上下文工程”系列教程对应的 Jupyter Notebook demo 代码。

仓库中的 Notebook 以文章内容为基础整理而成，既保留系列文章中的核心讲解，也补充了可运行的示例代码，方便读者在本地边看边跑，理解上下文工程在 Agent 系统中的实际落地方式。

## 仓库内容

- `*.ipynb`：系列文章对应的 Notebook 文件
- `requirements.txt`：本地运行 Notebook 所需依赖

## 环境准备

推荐使用 `conda` 创建独立环境运行这些 Notebook。

### 1. 进入仓库目录

```bash
cd "/Users/wuxucan/Documents/上下文系列文章/context-engineering-notebooks"
```

### 2. 创建 conda 环境

```bash
conda create -n context-engineering-notebook python=3.11 -y
```

### 3. 激活环境

```bash
conda activate context-engineering-notebook
```

### 4. 安装依赖

```bash
pip install -r requirements.txt
```

### 5. 注册 Jupyter 内核

注册后，你可以在 Jupyter 界面中直接选择这个 Python 环境来运行 Notebook。

```bash
python -m ipykernel install --user --name context-engineering-notebook --display-name "Python (context-engineering-notebook)"
```

## 如何运行 Notebook

### 启动 Jupyter Lab

```bash
jupyter lab
```

启动后，在浏览器中打开需要运行的 `.ipynb` 文件，选择内核 `Python (context-engineering-notebook)`，然后执行 Notebook 中的代码单元。

### 直接打开某个 Notebook

例如当前仓库中的示例文件：

```bash
jupyter lab "第二篇demo-system-prompt-instructions.ipynb"
```

如果你更习惯经典 Notebook 界面，也可以使用：

```bash
jupyter notebook "第二篇demo-system-prompt-instructions.ipynb"
```

## 如何执行 Notebook 中的代码

打开 Notebook 后，常见的执行方式如下：

- 逐个运行代码单元：在单元中按 `Shift + Enter`
- 顺序运行整篇 Notebook：选择 `Run All`
- 修改某段示例代码后重新运行对应单元，观察输出变化

建议第一次打开某个 Notebook 时，直接执行一次 `Run All`，确认依赖环境和代码都能正常运行。

## 适用场景

这个仓库适合以下几类使用方式：

- 配合微信公众号系列文章阅读，边看边运行 demo
- 作为学习上下文工程的实验记录和示例集合
- 后续持续积累“System Prompt、Instructions、User Input、Structured I/O、RAG、Tool Integration”等主题对应的 Notebook

## 说明

- Notebook 里的示例代码以教学演示为主，重点是帮助理解上下文工程设计方法
- 不同文章对应的 Notebook 可能包含伪代码、结构化示例、上下文组织策略和轻量实验代码
- 后续新增系列文章时，会继续向这个仓库补充对应的 `.ipynb` 文件
