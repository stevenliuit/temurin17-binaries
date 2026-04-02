# Temurin JDK 17 自动编译

[![Build Temurin JDK 17](https://github.com/stevenliuit/temurin17-binaries/actions/workflows/build-temurin.yml/badge.svg)](https://github.com/stevenliuit/temurin17-binaries/actions/workflows/build-temurin.yml)
[![GitHub release](https://img.shields.io/github/release/stevenliuit/temurin17-binaries.svg)](https://github.com/stevenliuit/temurin17-binaries/releases)
[![License](https://img.shields.io/badge/license-GPLv2%20with%20Classpath%20Exception-blue.svg)](https://openjdk.org/legal/gplv2+ce.html)

## 🎯 项目说明

这是 **Eclipse Temurin JDK 17** 的自动构建项目，支持：

- ✅ 编译任何 Temurin 17 版本（`jdk-17.0.18+8`, `jdk-17.0.19+8` 等）
- ✅ 自动同步上游所有标签
- ✅ 支持所有版本标签触发编译
- ✅ 自动下载和发布 Temurin JDK

## 📦 Temurin 17 版本格式

Temurin 使用以下版本格式：

```
jdk-17.0.18+8    # JDK 17.0.18 更新 8
jdk-17.0.19+8    # JDK 17.0.19 更新 8
jdk-17.0.17+10   # JDK 17.0.17 更新 10
```

## 🚀 快速使用

### 下载预编译的 JDK

访问 [Releases](https://github.com/stevenliuit/temurin17-binaries/releases) 页面下载：

| 平台 | 架构 | 文件 |
|------|------|------|
| Linux | x64 | `OpenJDK17U-jdk_x64_linux_hotspot_17.0.18+8.tar.gz` |
| Windows | x64 | `OpenJDK17U-jdk_x64_windows_hotspot_17.0.18+8.zip` |
| macOS | x64 | `OpenJDK17U-jdk_x64_mac_hotspot_17.0.18+8.tar.gz` |
| macOS | aarch64 | `OpenJDK17U-jdk_aarch64_mac_hotspot_17.0.18+8.tar.gz` |

### 手动触发编译

1. 访问 [Actions](https://github.com/stevenliuit/temurin17-binaries/actions/workflows/build-temurin.yml)
2. 点击 "Run workflow"
3. 输入要编译的版本标签：
   - `jdk-17.0.18+8` (最新稳定版)
   - `jdk-17.0.19+8` (下一个版本)
   - 任何其他标签
4. 点击 "Run workflow"

## 📋 可用版本

### 最新版本

| 版本 | 标签 | 状态 |
|------|------|------|
| JDK 17.0.19 | `jdk-17.0.19+8` | 最新 |
| JDK 17.0.18 | `jdk-17.0.18+8` | 稳定 |
| JDK 17.0.17 | `jdk-17.0.17+10` | 稳定 |
| JDK 17.0.16 | `jdk-17.0.16+8` | 稳定 |

### 查看所有标签

访问：https://github.com/adoptium/temurin17-binaries/tags

## 🔄 自动更新

### 定时同步

- **每 6 小时** 自动检查新版本
- **自动同步** 所有上游标签
- **自动触发** 新版本的编译构建

### Push 触发

推送标签时自动触发编译：

```bash
# 推送标签会自动触发构建
git push origin jdk-17.0.18+8
```

## 🔧 构建配置

### 支持的平台

- ✅ Linux x64
- ✅ Windows x64
- ✅ macOS x64
- ✅ macOS aarch64

### 构建类型

- `release` - 生产版本（默认）
- `fastdebug` - 快速调试版本
- `debug` - 完整调试版本

## 📊 构建状态

| 平台 | 状态 |
|------|------|
| Linux x64 | [![Linux x64](https://github.com/stevenliuit/temurin17-binaries/actions/workflows/build-temurin.yml/badge.svg?branch=main)](https://github.com/stevenliuit/temurin17-binaries/actions) |
| Windows x64 | [![Windows x64](https://github.com/stevenliuit/temurin17-binaries/actions/workflows/build-temurin.yml/badge.svg?branch=main)](https://github.com/stevenliuit/temurin17-binaries/actions) |
| macOS x64 | [![macOS x64](https://github.com/stevenliuit/temurin17-binaries/actions/workflows/build-temurin.yml/badge.svg?branch=main)](https://github.com/stevenliuit/temurin17-binaries/actions) |
| macOS aarch64 | [![macOS aarch64](https://github.com/stevenliuit/temurin17-binaries/actions/workflows/build-temurin.yml/badge.svg?branch=main)](https://github.com/stevenliuit/temurin17-binaries/actions) |

## 📝 使用方法

### Linux/macOS

```bash
# 下载并解压
tar -xzf OpenJDK17U-jdk_x64_linux_hotspot_17.0.18+8.tar.gz

# 设置环境变量
export JAVA_HOME=$PWD/jdk-17.0.18+8
export PATH=$JAVA_HOME/bin:$PATH

# 验证
java -version
```

### Windows

```powershell
# 下载并解压
Expand-Archive -Path OpenJDK17U-jdk_x64_windows_hotspot_17.0.18+8.zip -DestinationPath C:\jdk17

# 设置环境变量
$env:JAVA_HOME = "C:\jdk17\jdk-17.0.18+8"
$env:Path += ";C:\jdk17\jdk-17.0.18+8\bin"

# 验证
java -version
```

## 🔗 相关链接

- [Eclipse Temurin 官网](https://adoptium.net/)
- [Temurin 17 发布页](https://github.com/adoptium/temurin17-binaries/releases)
- [Temurin 17 源码](https://github.com/adoptium/temurin17-binaries)
- [OpenJDK 17](https://openjdk.org/projects/jdk/17/)

## 🆚 OpenJDK vs Temurin

| 项目 | 仓库 | 版本格式 | 说明 |
|------|------|---------|------|
| **OpenJDK 17** | openjdk/jdk17 | `jdk-17+35` | 官方 OpenJDK |
| **Temurin 17** | adoptium/temurin17-binaries | `jdk-17.0.18+8` | Eclipse 基金会构建 |

### 版本对应关系

| OpenJDK 标签 | Temurin 标签 | 版本 |
|--------------|-------------|------|
| `jdk-17+35` | `jdk-17.0.1+11` | JDK 17.0.1 |
| `jdk-17+36` | `jdk-17.0.2+8` | JDK 17.0.2 |
| - | `jdk-17.0.18+8` | JDK 17.0.18 (最新) |
| - | `jdk-17.0.19+8` | JDK 17.0.19 (最新) |

## 📄 许可证

Temurin JDK 使用 **GPLv2 with Classpath Exception** 许可证。

---

**Star ⭐ 本项目以获取最新构建通知！**