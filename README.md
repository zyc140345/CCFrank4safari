# CCFrank4safari

[CCF4dblp](https://github.com/WenyanLiu/CCFrank4dblp) 是一款浏览器插件，支持在 dblp、Google 学术、Connected Papers、Semantic Scholar 和 Web of Science 的搜索结果中显示中国计算机学会推荐的国际会议和期刊排名。

但该插件仅兼容 Chrome、Firefox 和 Edge，对习惯使用 Safari 的同学造成了不便。为了在 Safari 中使用 CCF4dblp，可以借助 Apple 官方提供的 [safari-web-extension-converter](https://developer.apple.com/documentation/safariservices/safari_web_extensions/converting_a_web_extension_for_safari) 工具进行转换，具体步骤如下：
1. 安装 [Xcode](https://apps.apple.com/us/app/xcode/id497799835)
2. 克隆原仓库
```shell
git clone https://github.com/WenyanLiu/CCFrank4dblp.git
```
3. 编辑 manifest.json 文件，将 manifest_version 字段修改为 2
4. 使用 safari-web-extension-converter 将原工程转换为 Xcode 工程
```shell
xcrun /Applications/Xcode.app/Contents/Developer/usr/bin/safari-web-extension-converter <仓库目录>
```
5. 转换成功后会自动打开 Xcode 工程，点击 CCFrank.xcodeproj，将两个以 (macos) 结尾的 TARGETS 中的 Signing & Capabilities/Team 字段改为自己的开发者账号（无需付费账号）
6. 选择 CCFrank (macos) 作为运行目标，点击运行按钮进行编译
7. 在打开的窗口中根据提示前往 Safari 添加并启用扩展
8. 初次启用时工具栏上会显示警告图标，需要点击拓展按钮进行授权
## 参考
1. <https://github.com/LSX-s-Software/CCF-Rank-Safari>
2. <https://github.com/WenyanLiu/CCFrank4dblp/issues/29#issuecomment-1008868397>