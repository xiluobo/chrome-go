<div align="center">

# ChromeGo

A Python-based tool for collecting and transforming Chrome proxy data for local testing, extraction, subscription generation, and data processing.

Maintained by xiluobo

[中文](README.md) | **English**

</div>

## Project Overview

This project is used to collect, organize, and export Chrome-related proxy data. It supports converting scraped results into common proxy subscription formats for local usage, debugging, and secondary processing.

This repository is now maintained as a personal project with the following goals:

- Provide a stable local execution entry point
- Support proxy data extraction and organization
- Export commonly used formats such as Clash, Base64, and URL lists
- Allow easy custom development and extension

## Features

- Automated collection of target data sources
- Filtering and aggregation of raw proxy records
- Exporting multiple common subscription formats
- Support for local script execution and custom configuration
- Suitable for learning, testing, and internal tool development

## Project Structure

```text
.
├── main.py                # Main entry script
├── requirements.txt       # Python dependencies
├── LICENSE                # MIT license
├── README.md              # Chinese documentation
├── README_EN.md           # English documentation
├── outputs/               # Exported output directory
├── templates/             # Template files
├── urls/                 # URL target files or rules
├── GeoLite2-City.mmdb    # GeoIP data file
└── .github/               # GitHub configuration
```

## Requirements

- Python 3.9+
- pip
- Network access for fetching source data

## Installation

```bash
git clone https://github.com/xiluobo/chrome-go.git
cd chrome-go
python -m venv .venv
source .venv/bin/activate  # Linux / macOS
# or .venv\Scripts\activate  # Windows
pip install -r requirements.txt
```

## Usage

```bash
python main.py
```

After running, the script generates output files in the `outputs/` directory based on the current configuration. You can also modify the target addresses, filtering rules, output format, and save path as needed.

## Common Output Files

Depending on the script configuration, the project may generate files such as:

- `clash_meta.yaml`
- `clash_meta_warp.yaml`
- `base64.txt`
- `proxy_urls.txt`

## Customization

If you want to adapt this project to your own use case, you can extend it by:

1. Changing the data source URL
2. Adjusting the filtering logic
3. Customizing the export format
4. Adding caching or logging
5. Integrating with other processing workflows

## Disclaimer

This project is intended for learning, research, and lawful technical validation only. Users are responsible for complying with the laws, regulations, and usage policies applicable in their region and network environment.

The author is not liable for any consequences arising from the use of this project, including but not limited to data loss, service disruptions, compliance risks, or network restrictions.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

If needed, I can continue helping turn this repository into a more complete personal project, such as:

- a Python CLI tool
- a web dashboard
- a data collection and visualization app
- a more branded personal project structure

Tell me the target direction and I can continue adapting it.
