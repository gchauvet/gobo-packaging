# Gobo Eiffel packaging

Meta project built on top of gobo eiffel project. Goal is to provide a way to package Gobo Eiffel (and libraries) to several platforms. The current version focus Linux Debian based distribution.

## Usage

```sh
git clone https://github.com/gchauvet/gobo-packaging.git
cd gobo-packaging
export GOBO_PACKAGING=`pwd`
```

### Build gobo provided as submodule (sources directory).
```sh
cd $GOBO_PACKAGING/sources
git submodule update --init --recursive # if no sources code available
git checkout tags/gobo-3.9
mkdir bin
export GOBO=`pwd`
cd work/bootstrap
```
Please refere to [sources/work/bootstrap/Readme.txt](sources/work/bootstrap/Readme.txt) to see how to bootstrap Gobo.

Check that 8 Gobo tools are present in sources/bin directory :
```sh
ls $GOBO_PACKAGING/sources/bin/ge*
```

### Build package to debian packager
```
cmake -G "<a generator>"
make package
```
