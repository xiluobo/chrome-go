<div align="center">

# ChromeGo

一个基于 Python 的 Chrome 代理信息收集与转换工具，适合本地测试、数据提取、订阅生成和代理数据处理。

由 xiluobo 维护与更新

**中文** | [English](README_EN.md)

</div>

## 项目简介

本项目用于收集、整理与导出 Chrome 相关代理数据，支持将抓取结果整理为常见的代理订阅格式，便于本地使用、调试和二次加工。

本仓库已按个人项目方式维护，核心目标是：

- 提供稳定的本地运行入口
- 支持提取与整理代理数据
- 输出 Clash / Base64 / URL 等常见格式
- 便于二次开发和自定义扩展

## 功能特点

- 自动采集目标数据源
- 过滤与聚合原始代理记录
- 输出多种常见订阅格式
- 支持本地脚本运行和自定义配置
- 适合学习、测试与内部工具化使用

## 目录结构

```text
.
├── main.py                # 主入口脚本
├── requirements.txt       # Python 依赖
├── LICENSE                # MIT 开源许可证
├── README.md              # 中文说明
├── README_EN.md           # 英文说明
├── outputs/               # 导出结果目录
├── templates/             # 模板文件
├── urls/                 # 目标链接或规则
├── GeoLite2-City.mmdb    # GeoIP 数据文件
└── .github/               # GitHub 配置
```

## 环境要求

- Python 3.9+
- pip
- 可联网访问以获取源数据

## 安装

```bash
git clone https://github.com/xiluobo/chrome-go.git
cd chrome-go
python -m venv .venv
source .venv/bin/activate  # Linux / macOS
# 或 .venv\Scripts\activate  # Windows
pip install -r requirements.txt
```

## 运行方式

```bash
python main.py
```

运行后，脚本会根据配置生成结果并写入 `outputs/` 目录中。你也可以根据需要修改脚本中的目标地址、过滤规则、输出格式或保存路径。

## 常见输出

项目中会生成以下类型的输出文件，具体取决于脚本配置：

- `clash_meta.yaml`
- `clash_meta_warp.yaml`
- `base64.txt`
- `proxy_urls.txt`

## 自定义说明

如果你希望将此项目用于自己的场景，可以根据以下方式进行扩展：

1. 修改数据源 URL
2. 调整过滤逻辑
3. 自定义导出格式
4. 增加本地缓存或日志
5. 接入其他处理流程

## 免责声明

本项目仅用于学习、研究和合法场景下的技术验证。使用者应自行遵守所在地区、网络环境和服务商的法律法规与使用规范。

作者不对因使用本项目造成的任何后果承担责任，包括但不限于数据丢失、网络封禁、合规风险或服务异常。

## 许可证

本项目采用 MIT License。详细内容请查看 [LICENSE](LICENSE)。

---

如果你需要，我也可以继续帮你把这个仓库进一步改造成：

- 一个完整的 Python CLI 项目
- 一个 Web 管理后台
- 一个代理数据抓取与可视化工具
- 一个更适合你个人品牌的仓库结构

你也可以直接告诉我你想做成哪种项目类型，我继续帮你落地。
