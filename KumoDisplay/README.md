# KumoDisplay 更新目录

此目录只服务 KumoDisplay，不与仓库中的其他软件共享清单、更新资产或版本号。

`0.2.0` 和 `0.2.1` 的历史 ZIP 内仍是 `KumoHiDPI.app` 及旧身份，仅为保留历史资产和签名，不是 KumoDisplay 的手动迁移安装包；`0.2.x` 用户必须另行手动安装正式 KumoDisplay。

- `KumoDisplay/appcast.xml`：KumoDisplay 客户端读取的 Sparkle 更新清单。
- `KumoDisplay/releases/<版本>/KumoDisplay-<版本>.zip`：该版本的完整更新包。
- `KumoDisplay/releases/<版本>/*.delta`：仅在存在已发布旧版本且 Sparkle 能生成有效增量时提供；首个版本不得伪造增量包。
- Sparkle EdDSA 签名使用钥匙串账户 `kumodisplay-ed25519`；私钥不得写入仓库或发布资产。

版本目录和其中资产一经发布即不可覆盖；任何修订必须使用更高的显示版本和构建号。发布时必须先写入并验证不可变版本资产，确认可匿名下载后，最后再更新 `KumoDisplay/appcast.xml`。

其他软件必须使用各自的顶级目录，禁止修改、复用或引用本目录中的清单和资产。
