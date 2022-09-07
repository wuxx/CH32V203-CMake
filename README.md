# CH32V203-CMake

摆脱eclipse编译环境，使用vscode编辑代码。

此仓库为cmake模板，请根据自己的工程进行适当修改。

请在CmakeLists.txt文件内更改`TOOLPATH`的变量为你的工具链路径。

```shell
A和B方法任选其一即可

A、使用cmake生成eclipse Makefile工程
cmake -G"Eclipse CDT4 - Unix Makefiles" ..
如果没有把make.exe加入系统path:
cmake -G"Eclipse CDT4 - Unix Makefiles" -D"你的路径/make.exe"  ..

B、使用cmake生成ninja工程
cmake -G"Ninja" ..
如果没有把ninja.exe加入系统path:
cmake -G"Ninja" -D"你的路径/ninja.exe" ..
```

## Linux 下使用说明
### 部署工具链环境
可在此处下载工具链 https://github.com/xpack-dev-tools/riscv-none-embed-gcc-xpack/releases
```
$tar -zxvf xpack-riscv-none-embed-gcc-10.2.0-1.2-linux-arm64.tar.gz
$export PATH=${PATH}:/your-toolchain-dir-path/xpack-riscv-none-embed-gcc-10.2.0-1.2/bin
```

### 安装ninjia构建工具
```
$sudo apt-get install ninja-build
```
### 编译
```
$./build.sh
```

