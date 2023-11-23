
# 自动抓取合并互联网上的公开节点。

## 关于 Google Play 等服务在国内无法使用的解决方法

由于 Google 调整了服务器安排，将原有的国外服务器的**域名**调整到了国内专版，但是**服务器**还没跟上，导致 Google Play 等服务在国内连上的是**空域名**，直接不能用了。当前的解决办法有：

1. **正常更新本项目的 Clash 订阅**，我们将 `googleapis.cn` 强制走了代理，让 Google Play 继续使用国外服务器，部分网络架构（如本机运行 Clash For Android）下服务能够恢复正常。如果您使用的是本项目提供的规则片段，请在 `rules` 开头加上：
```yaml
  - DOMAIN-SUFFIX,googleapis.cn,🚀 选择代理
  - DOMAIN-SUFFIX,xn--ngstr-lra8j.com,DIRECT # Google Play 国外/国内 服务器
  - DOMAIN-SUFFIX,xn--ngstr-cn-8za9o.com,DIRECT # Google Play 纯国内 服务器，尚未完成部署
```
2. **如果方案 1 无效，且你的手机已 ROOT，请解除 GMS 锁区**，安装 Magisk 模块 [Unlock-cn-gms](https://github.com/fei-ke/unlock-cn-gms)（[zip 下载](https://github.com/fei-ke/unlock-cn-gms/releases/download/v3.4/unlock-cn-gms-v3.4.zip)），这不一定适合所有手机，请先关注您手机中相关锁区文件的位置。
3. **如果你的手机未 ROOT，请使用 Clash For Android 试一试**，有概率正常。
4. 实在不行就等等吧，但愿 Google 能尽快修复此问题。

如果此问题有进展，我们会在此更新，请及时关注。

注意：原有的链接 1 出现过问题，我们在它前面添加了新的链接 1 并下移了原有链接。我们建议您将订阅链接改为新的加速链接 1。加速链接 3/4 含有缓存，可能不是最新，且访问速度没有链接 1 快。

我们新增了 `snippets` 文件夹来存放从 `list.yml` 中拆分出的配置片段，用于将本项目提供的一些配置整合到你自己的配置中。

此项目现已添加“反 996 许可证”，请各位使用者**不要违法违规要求别人加班，自觉遵守《中华人民共和国劳动法》及其它法律法规**！

## 使用方法

添加 Base64 订阅：
- [原始链接](https://rftti.space/freeVM/list.txt)
- [加速链接 4](https://cdn.staticaly.com/gh/peasoft/NoMoreWalls/master/list.txt)

或添加 Clash 订阅：
- [加速链接 1](https://rftti.space/freeVM/list.yml)
- [加速链接 5](https://raw.kgithub.com/peasoft/NoMoreWalls/master/list.yml)

# Windows 刷新 DNS
 
```shell
ipconfig /flushdns
```

## 免责声明

订阅节点仅作学习交流使用，用于查找资料，学习知识，不做任何违法行为。所有资源均来自互联网，仅供大家交流学习使用，出现违法问题概不负责。**做出违法行为需要承担法律责任，侥幸逃脱是不可能的**！为阻止违法行为，本项目随时可以停止运行！！！
