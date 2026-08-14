# RIA Skills

RIA 团队维护的 Agent Skills 集合。

## 可用 Skills

| Skill | 用途 |
| --- | --- |
| `ria-modern-paper` | 开发 RIA/ZTH 风格的现代 Paper/Folia 插件，涵盖版本策略、异步性能、Adventure、Folia 调度器、数据持久化、命令权限和游戏内消息样式。 |

## 安装

需要提前安装 [Node.js](https://nodejs.org/) 和 Git。Skills 通过 [`npx skills`](https://skills.sh/) 安装。

### SSH（推荐）

推荐在已配置 GitHub SSH 密钥的开发机上使用 SSH 地址。在国内网络环境中优先尝试这种方式；如果当前网络无法连接 GitHub SSH，再使用后面的 HTTPS 地址。

```bash
npx skills add git@github.com:RIA-AED/skills.git \
  -g \
  -s ria-modern-paper \
  -y
```

可以先检查 SSH 是否可用：

```bash
ssh -T git@github.com
```

### HTTPS（备用）

未配置 SSH 密钥时，可以改用 HTTPS：

```bash
npx skills add https://github.com/RIA-AED/skills.git \
  -g \
  -s ria-modern-paper \
  -y
```

`-g` 表示安装到用户级全局 Skills 目录；`-s` 用于选择仓库中的指定 Skill。

OMP 会从全局 `~/.agents/skills` 目录加载 Skills。安装完成后，请新建 OMP 会话以加载新 Skill；已经打开的会话不会热加载。

## 检查安装

```bash
npx skills list -g
```

列表中应出现：

```text
ria-modern-paper
```

## 更新

```bash
npx skills update ria-modern-paper -g -y
```

## 卸载

```bash
npx skills remove ria-modern-paper -g -y
```
