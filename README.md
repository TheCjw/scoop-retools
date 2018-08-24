# scoop-retools [![Build status](https://ci.appveyor.com/api/projects/status/prkvjafc09jbapw4?svg=true)](https://ci.appveyor.com/project/TheCjw/scoop-retools)

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

### Bulid [WinAFL](WinAFL)

```bash
scoop install dynamorio
git clone https://github.com/ivanfratric/winafl
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