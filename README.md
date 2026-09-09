# FastAPI 自动化测试完整项目

这是一个从零开始学习自动化测试的完整项目，包含 **API 接口测试**、**Web 自动化测试** 和 **HTML 测试报告生成**。

## 📚 项目结构

```
fastapi-automation-testing/
├── app/                          # FastAPI 应用代码
│   ├── main.py                  # 主应用入口
│   ├── models.py                # 数据模型
│   └── crud.py                  # 业务逻辑
├── tests/                        # 测试代码
│   ├── test_api.py              # API 接口测试
│   ├── test_web.py              # Web 自动化测试
│   ├── conftest.py              # Pytest 配置和 fixtures
│   └── test_data/               # 测试数据
├── docs/                         # 文档
│   ├── API_TESTING_GUIDE.md     # API 测试教程
│   └── WEB_TESTING_GUIDE.md     # Web 测试教程
├── reports/                      # 测试报告输出目录
├── .github/workflows/            # GitHub Actions CI/CD
├── requirements.txt              # 项目依赖
├── pytest.ini                    # Pytest 配置文件
└── README.md                     # 项目说明
```

## 🚀 快速开始

### 1. 安装依赖

```bash
pip install -r requirements.txt
```

### 2. 运行 FastAPI 应用

```bash
uvicorn app.main:app --reload --port 8000
```

应用将在 `http://localhost:8000` 启动

### 3. 运行测试

#### 运行所有测试
```bash
pytest -v --html=reports/report.html --self-contained-html
```

#### 只运行 API 测试
```bash
pytest tests/test_api.py -v
```

#### 只运行 Web 测试
```bash
pytest tests/test_web.py -v
```

#### 运行带覆盖率的测试
```bash
pytest --cov=app tests/ --html=reports/report.html --self-contained-html
```

## 📖 学习内容

### 第1部分：准备工作 ✅
- [x] 项目结构设计
- [x] 环境配置
- [x] 依赖安装

### 第2部分：构建 FastAPI 应用
- 创建简单的 REST API
- 实现数据模型和业务逻辑
- 添加数据库操作

### 第3部分：API 接口自动化测试
- Requests 库基础
- 参数化测试 (parametrize)
- 数据驱动测试
- 前置/后置处理 (Setup/Teardown)

### 第4部分：Web 自动化测试
- Selenium 基础
- 元素定位策略
- 等待机制 (显式/隐式等待)
- Page Object 模式

### 第5部分：测试报告
- pytest-html 报告生成
- 测试覆盖率 (Coverage)
- 报告定制和美化

### 第6部分：持续集成
- GitHub Actions 配置
- 自动化测试流程
- 通知和报告

## 🎯 核心命令速查

| 命令 | 说明 |
|------|------|
| `pytest -v` | 详细模式运行所有测试 |
| `pytest -v --tb=short` | 简短的错误追踪 |
| `pytest tests/test_api.py::test_create_user -v` | 运行特定测试 |
| `pytest -k "test_get" -v` | 按名字过滤测试 |
| `pytest --collect-only` | 只显示测试不运行 |
| `pytest -x` | 遇到第一个失败就停止 |
| `pytest --lf` | 只运行上次失败的测试 |
| `pytest -n auto` | 并行运行测试 (需要 pytest-xdist) |

## 🔗 相关资源

- [FastAPI 官方文档](https://fastapi.tiangolo.com/)
- [Pytest 官方文档](https://docs.pytest.org/)
- [Requests 文档](https://docs.python-requests.org/)
- [Selenium 文档](https://selenium.dev/documentation/)

## 📝 学习笔记

在学习过程中可以在本项目的 `docs/` 目录下查看详细的教程和笔记。

## 💡 提示

- 确保已安装 Python 3.8+
- 建议使用虚拟环境 (venv)
- Web 测试需要 Chrome/Firefox 浏览器
- 测试报告会生成在 `reports/` 目录

---

**开始学习吧！** 🎉
