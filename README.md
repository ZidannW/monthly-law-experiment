# ZidanW. · Monthly Law Experiment

一个仅需静态托管、为 30 天法硕互动备考设计的私人学习记录网站。

## 立即使用

直接打开 `index.html`，或通过本地 HTTP 服务预览：

```bash
python3 -m http.server 8000
```

随后打开 http://localhost:8000 。

## 发布到 GitHub Pages

1. 在自己的 GitHub 账号创建仓库 `monthly-law-experiment`。
2. 将本文件夹内 `index.html`、`README.md`、`.nojekyll` 上传至仓库根目录并提交。
3. 打开仓库 **Settings → Pages → Build and deployment**，Source 选择 **Deploy from a branch**，Branch 选 `main` / `/(root)`，点击 Save。
4. GitHub 发布成功后，若 GitHub 用户名是 `zidanw`，网址通常为 `https://zidanw.github.io/monthly-law-experiment/`。否则使用自己真实的 GitHub 用户名。

## ChatGPT 对话如何更新网站

网站的 **聊天同步与备份** 页面有一份可复制给 ChatGPT 的同步指令。每次结束一段学习对话：

1. 在 ChatGPT 中粘贴该指令，让它**只根据实际聊过的内容**输出 JSON；
2. 复制 JSON 到网站的导入区域，点击“导入并合并记录”；
3. 网站立刻更新学习日志、知识图谱和待复习列表。不同设备之间，可导出完整备份 JSON、再导入。

> V1 **不会自动读取 ChatGPT 聊天**，也不具备后台定时同步。网站刷新时会自动重新计算实验天数和复习到期情况，但新增聊天学习内容需要主动同步。不要把导出的私人学习数据提交到公开 GitHub 仓库。

## 数据和隐私

- 所有学习数据保存在当前浏览器的 localStorage；它不自动跨设备同步，清理浏览器数据也可能将其删除。
- 建议每日或每周下载 JSON 备份并妥善保管。
- GitHub Pages 网站代码可以公开访问，localStorage 中的本地学习记录**不会随代码上传**。
- 网站暂未实现身份认证，不要把私人记录写进网页源码。
- 首次打开使用空白真实数据，不伪造错题、学习时长和掌握率。

## 数据格式

参见 `sample-sync.json`，该文件是字段演示，并不包含真实学习成果。导入时请使用由真实学习对话产生的数据。
