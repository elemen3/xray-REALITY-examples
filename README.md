**推荐使用：** 

:rocket:VLESS-XTLS-Vision

:rocket:VLESS-XTLS-uTLS-REALITY

:+1:**XTLS Vision [简介](https://github.com/XTLS/Xray-core/discussions/1295) [安装指南](https://github.com/chika0801/Xray-install)**

:+1:**REALITY [设计哲学](https://github.com/XTLS/Xray-core/issues/1689#issuecomment-1439447009) [配置模板说明](https://github.com/XTLS/REALITY#readme) [安装指南](https://github.com/chika0801/Xray-install/blob/main/REALITY.md)**

~~REALITY需要使用[最新测试版本](https://github.com/XTLS/Xray-core/actions/workflows/release.yml)的Xray-core文件~~

或者[自己编译](https://github.com/chika0801/Xray-install/blob/main/compile_Xray-core.md)使用最新源码的Xray-core文件

**希望你为[REALITY](https://github.com/XTLS/REALITY)仓库点一个:star:**

~~[我们定个新的小目标：REALITY stars 到 1024 当天出文章](https://github.com/XTLS/Xray-core/issues/1679#issuecomment-1436520973)~~

:eyes:**Xray-core need you help!**

**:star:Star [this project](https://github.com/XTLS/REALITY) to make the next future a REALITY.**

**使用提醒：** 

:exclamation:相对于 XTLS Vision 的使用基数，目前几乎没有收到 **配置正确** 的 Vision 被封端口的报告，**配置正确** 指的是：

1. 服务端使用合理的端口，禁回国流量
2. 只配置 XTLS Vision，不兼容普通 TLS 代理
3. 回落到网页，不回落/分流到其它代理协议
4. 客户端启用 uTLS（fingerprint） [#1](https://github.com/XTLS/Xray-core/issues/1544#issuecomment-1399194727)

:exclamation:首先，如果你特别不想被封，**请先选择一个干净的 IP**，并按照 **配置正确** 去搭建、使用 XTLS Vision。

**但是，即使你这样做了，也无法保证 100% 不被封**。自去年底始，很多人的未知流量秒封 IP，TLS in TLS 流量隔天封端口。XTLS Vision 不是未知流量，且完整处理了 TLS in TLS 特征，目前看来效果显著。**但这并不意味着，用 XTLS Vision 可以 100% 不被封，认识到这一点是非常、非常重要的，不要自己偶然被封就大惊小怪**。

**因为除了协议本身，还有很多角度能封你**。以 IP 为例，你无法保证 IP 真的干净，无法避免被邻居波及，无法避免整个 IP 段被重点拉清单。也有可能某些地区的 GFW 有独特的标准，比如某个 IP 只有寥寥数人访问连却能跑那么多流量，封。**如果你的 XTLS Vision 被封了，但没有出现去年底 TLS 那样的大规模被封报告，我真心建议你换端口、换 IP、换服务商依次试一遍**。 [#2](https://github.com/XTLS/Xray-core/issues/1544#issuecomment-1402118517)

:exclamation:如果你之前用了其它协议导致 TCP/443 端口被封，**Vision 并没有“解封已经被封的端口”的能力**，换个 IP 或端口 [#3](https://github.com/XTLS/Xray-core/issues/1670#issuecomment-1436240888)

:exclamation:看来好多人还不知道代码里 Vision 只支持纯净入站或另一个 Vision 入站，~~当然要改也是不难的~~ [#4.1](https://github.com/XTLS/Xray-core/issues/1612#issuecomment-1418829266)

其实我早就看到了这个问题 [#1500](https://github.com/XTLS/Xray-core/issues/1500) ，~~只是不想改~~

因为根据历史，机场会用 SS 或 VMess 中转 XTLS 出墙，XTLS 把苦力活全干了，还给 GFW 喂了大量数据，却对社区没有任何帮助
我觉得这样并不好，所以我不会去改它，当然 PR is acceptable [#4.2](https://github.com/XTLS/Xray-core/issues/1612#issuecomment-1418880212)
