<div align="center">

# ChromeProxy Studio

Chrome 代理数据采集与转换工具

由 xiluobo 维护与更新

**中文** | [English](README_EN.md)

</div>

## 项目简介

ChromeProxy Studio 是一个基于 Python 的 Chrome 代理数据采集与转换工具，适合本地测试、代理数据整理、订阅生成和二次开发。

本项目已从原始 Fork 代码基础上重构为个人维护版本，核心目标是：

- 提供稳定的本地运行入口
- 收集并整理 Chrome 相关代理信息
- 支持输出常见订阅格式
- 便于自定义扩展与二次开发

## 功能特点

- 自动抓取目标数据源
- 清洗、过滤与聚合代理记录
- 导出 Clash、Base64、URL 等常见格式
- 支持本地脚本运行与自定义配置
- 适合研究、测试与内部工具化使用

## 目录结构

```text
.
├── main.py                # 主入口脚本
├── requirements.txt       # Python 依赖
├── LICENSE                # MIT 开源许可证
���── README.md              # 中文说明
├── README_EN.md           # 英文说明
├── outputs/               # 输出目录
├── templates/             # 模板文件
├── urls/                 # 目标链接或规则
├── GeoLite2-City.mmdb    # GeoIP 数据文件
├── .github/               # GitHub 配置
└── .gitignore             # Git 忽略配置
```

## 环境要求

- Python 3.9+
- pip
- 可联网访问以获取数据源

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

运行后，脚本会根据当前配置生成结果，并输出到 `outputs/` 目录中。你也可以根据需要修改数据源、过滤规则、导出格式和保存路径。

## 常见输出

根据脚本配置，项目可能生成以下输出：

- `clash_meta.yaml`
- `clash_meta_warp.yaml`
- `base64.txt`
- `proxy_urls.txt`

## 自定义扩展

如果你希望把这个项目用于自己的业务场景，可以从以下方面扩展：

1. 修改数据源地址
2. 调整过滤逻辑
3. 自定义导出格式
4. 增加缓存、日志和监控
5. 接入更大规模的数据处理流程

## 免责声明

本项目仅用于学习、研究和合法场景下的技术验证。使用者需自行遵守所在地区、网络环境和服务商的法律法规与使用规范。

作者不对因使用本项目造成的任何后果承担责任，包括但不限于数据丢失、网络风险、合规风险或服务异常。

## 许可证

本项目采用 MIT License。详细内容请查看 [LICENSE](LICENSE)。

---

如果你需要，我也可以继续帮你把这个仓库进一步升级成更完整的个人项目，包括：

- 更清晰的 CLI 结构
- Web 管理后台
- 自动化采集流程
- 更统一的项目命名与模板
