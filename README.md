
# 🚀 快速配置 OpenWrt 本地编译环境

---

## ✨ 项目特性

✅ 自动安装所需依赖，省去手动配置烦恼  
🚀 一键初始化 OpenWrt 编译环境并开始构建  
🔄 支持中断后续编，智能跳过重复步骤  
♻️ 提供 `--reset` 参数，强制清空缓存重构  
🖥️ 测试编译基于 **Ubuntu 24.04**

---

## 🧰 环境准备

### 下载构建脚本

```bash
wget https://raw.githubusercontent.com/8680/OpenWrt-AutoBuild/refs/heads/master/diy/scripts/build_openwrt.sh
```

### 更新系统并安装依赖

```bash
sudo apt update -y
sudo apt full-upgrade -y
```

```bash
sudo apt install -y \
  ack antlr3 asciidoc autoconf automake autopoint binutils bison \
  build-essential bzip2 ccache clang cmake cpio curl device-tree-compiler \
  flex gawk gcc-multilib g++-multilib gettext genisoimage git gperf haveged \
  help2man intltool libc6-dev-i386 libelf-dev libfuse-dev libglib2.0-dev \
  libgmp3-dev libltdl-dev libmpc-dev libmpfr-dev libncurses5-dev \
  libncursesw5-dev libpython3-dev libreadline-dev libssl-dev libtool llvm \
  lrzsz msmtp ninja-build p7zip p7zip-full patch pkgconf python3 \
  python3-pyelftools python3-setuptools qemu-utils rsync scons squashfs-tools \
  subversion swig texinfo uglifyjs upx-ucl unzip vim wget xmlto xxd zlib1g-dev
```

---

## 🏗️ 编译流程

### 🔹 第一次运行（初始化 + 编译）

```bash
bash build_openwrt.sh
```

### 🔄 继续构建（跳过前置配置）

中途取消后再次运行，自动跳过前置步骤，继续编译：

```bash
bash build_openwrt.sh
```

### ♻️ 强制重构（清除缓存，重新开始）

如需清空缓存、从头开始构建：

```bash
bash build_openwrt.sh --reset
```

---

