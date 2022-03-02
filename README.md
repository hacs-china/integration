# HACS 极速版 

[HACS](https://hacs.xyz)是一款优秀的 [Home Assistant](https://www.home-assistant.io) 集成商店，然而国人想要使用它下载插件或前端卡片却困难重重，主要原因就是国内的网络环境。
本项目使用了[ghproxy.com](https://ghproxy.com)和[fastgit.org](https://fastgit.org)提供的Github镜像服务，可以让大家更快的下载商店里的插件。

## 安装

> 本项目是HACS官方集成的修改版，安装本项目版本会覆盖官方的集成，但是无需重新配置集成(共用一套配置)，因此你可以放心安装。如果想切换到官方版本，使用官方的shell命令再安装即可。

### 使用命令行安装(推荐)

```bash
wget -O - https://cdn.jsdelivr.net/gh/hasscc/get@main/get | DOMAIN=hacs REPO_PATH=hacs-china/integration ARCHIVE_TAG=china bash -
```

> 如果上面的命令执行后卡住不动，或没有提示安装成功，请尝试下面的命令

```bash
wget -O - https://cdn.jsdelivr.net/gh/hasscc/get@main/get | HUB_DOMAIN=ghproxy.com/github.com DOMAIN=hacs REPO_PATH=hacs-china/integration ARCHIVE_TAG=china bash -
```

- 如果是haos/hassio/supervisor版本的HA，可直接在宿主机或`Terminal & SSH`加载项中执行上面的命令
- 如果是core/docker版本的HA，需要ssh登陆宿主机后，并cd进入到HA配置目录再执行安装命令

### 手动安装

- [点击这里下载](https://github.com/hacs-china/integration/releases/latest/download/hacs.zip)安装包并解压 (如果下载不了请点[这里](https://ghproxy.com/github.com/hacs-china/integration/releases/latest/download/hacs.zip)或[这里](https://hub.fastgit.xyz/hacs-china/integration/releases/latest/download/hacs.zip))
- 通过samba/ftp进入HA配置目录
- 在HA配置目录下创建`custom_components`文件夹 (如果已有请忽略)
- 在`custom_components`目录下创建`hacs`文件夹 (如果已有请删除重新创建)
- 將解压出来的hacs文件复制到刚创建的`hacs`文件夹
- 重启HA
- [添加HACS集成](https://my.home-assistant.io/redirect/config_flow_start/?domain=hacs) (仅首次安装)


### 常见问题

- [极速版和官方HACS的差别有那些？](https://github.com/hacs-china/integration/compare/main...china)


------


# HACS (Home Assistant Community Store)

[![Total alerts](https://img.shields.io/lgtm/alerts/g/hacs/integration.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/hacs/integration/alerts/)
[![Language grade: Python](https://img.shields.io/lgtm/grade/python/g/hacs/integration.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/hacs/integration/context:python)
[![Downloads for latest release](https://img.shields.io/github/downloads/hacs/integration/latest/total.svg)](https://github.com/hacs/integration/releases/latest)

_Manage (Install, track, upgrade) and discover custom elements for Home Assistant directly from the UI._

![gif](https://raw.githubusercontent.com/hacs/documentation/master/static/img/demo.gif)

## What?

HACS is a integration that gives the user a powerful UI to handle downloads of custom needs.

**Highlights of what HACS can do:**

- Help you discover new custom elements.
- Help you download new custom elements.
- Help you keep track of your custom elements.
  - Manage(download/update/remove)
  - Shortcuts to repositories/issue tracker

## Useful links

- [General documentation](https://hacs.xyz/)
- [Configuration](https://hacs.xyz/docs/configuration/basic)
- [FAQ](https://hacs.xyz/docs/faq/what)
- [GitHub](https://github.com/hacs)
- [Discord](https://discord.gg/apgchf8)
- [Become a GitHub sponsor? ❤️](https://github.com/sponsors/ludeeus)
- [BuyMe~~Coffee~~Beer? 🍺🙈](https://buymeacoffee.com/ludeeus)


## Issues

~~If~~ When you experience issues/bugs with this the best way to report them is to open an issue in **this** repo.

[Issue link](https://hacs.xyz/docs/issues)
