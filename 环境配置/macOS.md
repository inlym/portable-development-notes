# macOS 开发机环境配置

## 初始化阶段

### 起步软件

#### Homebrew

##### 安装 Homebrew

使用以下命令安装 [Homebrew](https://brew.sh/zh-cn/) 。

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

输入以下命令查看版本号，验证安装成功。

```bash
brew -v
```

##### 切换为国内镜像

切换为清华镜像（当前该镜像更新最快、最稳定）

```bash
git -C "$(brew --repo)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles' >> ~/.zprofile
source ~/.zprofile
```

检查结果

```bash
brew update
brew config | grep HOMEBREW_BOTTLE_DOMAIN
```

## 安装软件阶段

### 使用 Homebrew 安装软件

以下是开发环境必备软件

| 软件                                                               | 安装命令                                    |
| ------------------------------------------------------------------ | ------------------------------------------- |
| [git](https://git-scm.com)                                         | `brew install git`                          |
| [Oracle Java](https://www.oracle.com/java/technologies/downloads/) | `brew install --cask oracle-jdk`            |
| [node](https://nodejs.org/)                                        | `brew install node`                         |
| [maven](https://maven.apache.org/)                                 | `brew install maven`                        |
| [nginx](https://nginx.org/)                                        | `brew install nginx`                        |
| [VS Code](https://code.visualstudio.com/)                          | `brew install --cask visual-studio-code`    |
| [Maple Mono NF CN](https://font.subf.dev/en/)                      | `brew install --cask font-maple-mono-nf-cn` |
| [Bruno](https://www.usebruno.com/)                                 | `brew install --cask bruno`                 |
| [Tabby](https://eugeny.github.io/tabby/)                           | `brew install --cask tabby`                 |
| [Redis Insight](https://redis.io/insight/)                         | `brew install --cask redis-insight`         |

以下是生活用途日常软件

| 软件                                            | 安装命令                            |
| ----------------------------------------------- | ----------------------------------- |
| [微信 Mac 版](https://mac.weixin.qq.com/)       | `brew install --cask wechat`        |
| [微信输入法](https://z.weixin.qq.com/)          | `brew install --cask wetype`        |
| [QQ](https://im.qq.com/macqq/index.shtml)       | `brew install --cask qq`            |
| [Snipaste](https://www.snipaste.com/)           | `brew install --cask snipaste`      |
| [Google Chrome](https://www.google.com/chrome/) | `brew install --cask google-chrome` |
| [Clash Party](https://clashparty.org/)          | `brew install --cask clash-party`   |
| [Obsidian](https://obsidian.md/)                | `brew install --cask obsidian`      |
| [Mac Mouse Fix](https://macmousefix.com/)       | `brew install --cask mac-mouse-fix` |

## 配置环境阶段

### 常规配置

#### git

配置全局用户信息

```bash
git config --global user.name "inlym"
git config --global user.email "inlym@qq.com"
```

生成 SSH 密钥对

```bash
ssh-keygen -t ed25519 -C "替换为当前主机名"
```

#### npm

替换为阿里源

```bash
npm config set registry=https://registry.npmmirror.com
```
