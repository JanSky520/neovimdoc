# neovimdoc

[TOC]

## 项目简介

此项目为 Neovim 的中文文档翻译项目，目前正在持续更新。欢迎大家加入！

![微信群二维码](./res/groupQR_code.jpg)

## 使用方法

***如果你使用 Snap 安装了 Neovim，那么一下配置可能不适合你。请先参考 (关于从 Snap 安装的 Neovim 的说明)[#关于从 Snap 安装的 Neovim 的说明]

使用 git 命令克隆本项目

```bash
git clone https://github.com/JanSky520/neovimdoc.git
```

切换到本项目的根文件夹
```bash
cd neovimdoc
```

在使用本项目提供的中文文档前，建议将原始英文文档进行备份

```bash
sudo cp -rf /usr/share/nvim/runtime/doc/ /usr/share/nvim/runtime/doc.bak
```

运行以下命令，使用本项目提供的中文文档

```bash
sudo cp -rf ./nvim_doc/* /usr/share/nvim/runtime/doc
```

运行成功后，进入 Neovim，输入 `:help` 命令，即可查看中文文档（多数文档仍待翻译）。


***注意：由于不是使用的插件替换方法，在更新neovim后可能变回英文，重新替换即可。***

---

如果想要恢复原始的英文文档，请使用

```bash
sudo cp -rf /usr/share/nvim/runtime/doc.bak/* /usr/share/nvim/runtime/doc
```

删除备份命令：

```bash
sudo rm -rf /usr/share/nvim/runtime/doc.bak
```

## 关于从 Snap 安装的 Neovim 的说明

经过测试，从 Snap 安装的 Neovim 貌似不能根据以上方法更改文档配置。

我们强烈建议你抛弃 Snap，以下是如何从 Snap 版 Neovim 迁移到 apt 版 Neovim 的步骤：

删除 Snap 版 Neovim

```bash
sudo snap remove nvim
```

添加 apt ppa 源

```bash
sudo add-apt-repository ppa:neovim-ppa/unstable
```

更新 apt

```bash
sudo apt update
sudo apt upgrade
```

使用 apt 安装 Neovim

```bash
sudo apt install neovim
```

安装完成后，输入 `nvim` 即可启动 Neovim。