# scoop-retools 

[![Build status](https://img.shields.io/appveyor/ci/TheCjw/scoop-retools/master.svg?style=flat-square&label=AppVeyor&logo=appveyor)](https://ci.appveyor.com/project/TheCjw/scoop-retools) [![LICENSE](https://img.shields.io/github/license/TheCjw/scoop-retools.svg?style=flat-square)](https://github.com/TheCjw/scoop-retools/blob/master/LICENSE) [![size](https://img.shields.io/github/repo-size/thecjw/scoop-retools.svg?style=flat-square)](https://github.com/TheCjw/scoop-retools) [![awesome](https://awesome.re/badge-flat.svg)](https://github.com/scoopinstaller/awesome-scoop)

Scoop bucket for reverse engineering tools.

## Usage

1. Install [scoop](https://github.com/lukesampson/scoop)

2. Add this bucket to scoop:
```bash
scoop bucket add retools https://github.com/TheCjw/scoop-retools.git
```
3. Install tools via `scoop install`:
```bash
scoop install smali baksmali apktool
```
4. Done.

## Using [DynamoRIO](https://www.dynamorio.org/)

### Bulid [WinAFL](https://github.com/googleprojectzero/winafl)

```bash
scoop install dynamorio
git clone https://github.com/googleprojectzero/winafl
cd winafl
# Compile 32bit tool
mkdir build32
cd build32
cmake .. -DDynamoRIO_DIR="$env:DYNAMORIO_DIR"
cmake --build . --config Release
# or 64bit
mkdir build64
cd build64
cmake .. -DDynamoRIO_DIR="$env:DYNAMORIO_DIR"
cmake --build . --config Release
```