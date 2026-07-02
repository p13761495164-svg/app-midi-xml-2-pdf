# MIDI / MusicXML Score Web App

一个独立网页版应用，用来上传 MIDI 或 MusicXML 文件，显示钢琴双谱表，并通过浏览器打印导出 PDF。

## 使用

```bash
python3 -m http.server 4173
```

然后打开：

```text
http://127.0.0.1:4173/
```

## 功能

- 上传 `.mid`、`.midi`、`.xml`、`.musicxml`
- MIDI 自动转换成高音谱号和低音谱号两行钢琴谱
- MusicXML 直接渲染为五线谱
- 可设置 MIDI 拆分音高、拍号和 16 分音符量化
- 点击“导出 PDF”，在系统打印窗口选择保存为 PDF

## 说明

页面使用 OpenSheetMusicDisplay 渲染谱面，浏览器需要能访问 jsDelivr CDN。MIDI 转谱是面向普通钢琴文件的简化转换，适合预览和打印；复杂多声部、踏板、力度、装饰音等不会完整还原。
