# 书荒阅读 · 发布仓

这个仓**只放发布产物**;代码在 https://github.com/shizheang/shuhuang 。

每次发版在这里建一个 Release,挂两个资产:

- `version.json` —— 应用「检查更新」读的清单(`version` / `notes` / `apk`)
- `app-arm64-release-signed.apk` —— 真机(arm64)安装包

应用读的是 `releases/latest/download/version.json` —— **github.com 域上的静态资产**,
不依赖 `api.github.com`(后者在部分网络下不可达)。

> 发布用 `node scripts/publish-release.mjs --publish`(在代码仓里跑)。
