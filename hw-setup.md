# AP1400-2作业环境配置

配置教程基于Linux或WSL
以下教程基于WSL

## 环境设置

1. 安装Linux-Ubuntu或WSL
2. Linux中安装cmake
3. vscode连接WSL

### 安装googletest

```bash
mkdir AP1400
cd AP1400

git clone https://github.com/google/googletest.git -b release-1.12.1
cd googletest   # Main directory of the cloned repository.
mkdir build     # Create a directory to hold the build output.
cd build
cmake ..        # Generate native build scripts for GoogleTest.
make
make install
```

### 获取作业源码

```bash
cd ../../AP1400
git clone https://github.com/courseworks/AP1400-2-HW1
```

### 编译和测试

安装googletest之后vscode连接WSL打开`AP1400/HW`文件时就不会报`gtest.h`头文件找不到的错误
代码编写完成后要测试是在`main.cpp`中将测试代码打开

在`AP1400/HW`目录下

```bash
mkdir build
cd build
cmake ..
make
```

编译成功后在`AP1400/HW/build`目录下执行

```bash
./main
```

结果显示PASSED即成功
