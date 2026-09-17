# RoboMaster CMake Hello World

一个使用 C++17 和 CMake 构建的最小 Hello World 项目。程序运行后精确输出：

```text
Hello, RoboMaster!
```

## 环境

- Ubuntu 22.04 LTS
- CMake 3.16 或更高版本
- 支持 C++17 的 C++ 编译器（如 GCC/G++）
- Git

Ubuntu 22.04 可用以下命令安装依赖：

```bash
sudo apt update
sudo apt install -y git cmake build-essential
```

## 获取、构建与运行

```bash
git clone https://github.com/JackyHu0314/RoboMaster.git
cd RoboMaster
cmake -S . -B build
cmake --build build
./build/hello
```

预期输出：

```text
Hello, RoboMaster!
```

## 验证

```bash
ctest --test-dir build --output-on-failure
```

GitHub Actions 会在 Ubuntu 22.04 上从干净检出状态执行配置、构建、测试和运行。

## 目录结构

```text
.
├── .github/workflows/build.yml  # Ubuntu 22.04 自动构建验证
├── src/main.cpp                 # C++ 程序入口
├── .gitignore                   # 排除 build/ 等生成物
├── CMakeLists.txt               # CMake 构建配置
└── README.md                    # 项目说明
```

## Ubuntu 22.04 构建证据

[查看实际构建与运行日志](https://github.com/JackyHu0314/RoboMaster/actions/runs/35083265854/job/104752040072)，包含 Ubuntu 22.04.5 LTS、构建成功和 `Hello, RoboMaster!` 输出。

<img width="1265" height="712" alt="clipboard" src="https://github.com/user-attachments/assets/6578627e-8cd6-4ba4-ad30-58dd0c0b703d" />
