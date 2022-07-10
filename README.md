![Logo](https://whitesource-resources.s3.amazonaws.com/ws-sig-images/Whitesource_Logo_178x44.png)  
[![License](https://img.shields.io/badge/License-Apache%202.0-yellowgreen.svg)](https://opensource.org/licenses/Apache-2.0)
[![CI](https://github.com/whitesource-ps/ws-sbom-generator/actions/workflows/ci.yml/badge.svg)](https://github.com/whitesource-ps/ws-sbom-generator/actions/workflows/ci.yml)
[![Python 3.8](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Blue_Python_3.8_Shield_Badge.svg/76px-Blue_Python_3.8_Shield_Badge.svg.png)](https://www.python.org/downloads/release/python-380/)
[![GitHub release](https://img.shields.io/github/v/release/whitesource-ps/ws-sbom-generator)](https://github.com/whitesource-ps/ws-sbom-generator/releases/latest)  

# WS Joint SBOM Tool in SPDX format
CLI Tool to generate joint SBOM report in [SPDX format](https://spdx.org) from two SBOM reports.
* The tool can generate mutual report from two SBOM reports in **JSON** format

## Prerequisites
Python 3.9+

### Installation and Execution by pulling package from PyPi:
1. Execute pip install `pip install ws-joint-spdx`
2. Run report: `ws_joint_spdx -f1 <FIRST_FILE> -f2 <SECOND_FILE> -o <OUTPUT_FILE> -hf <HEAD_FILE>`

### Required and Optional arguments:
```shell
  -h, --help            show this help message and exit
  -f1 FIRST_FILE, --first_file
                  FIRST_FILE
  -f2 SECOND_FILE, --second_file 
                  SECOND_FILE
  -hf HEAD_FILE, --head_file 
                  Scope token of SBOM report to generate
    -o OUTPUT_FILE, --output_file 
                  OUTPUT_FILE
```
## Examples:
```shell
# Create output report with head data from first file 
ws_joint_spdx -f1 <FIRST_FILE> -f2 <SECOND_FILE> -o <OUTPUT_FILE>

# Create output report with head data from second file 
ws_joint_spdx -f1 <FIRST_FILE> -f2 <SECOND_FILE> -o <OUTPUT_FILE> -hf False

```