# PhotoMind v1.0（Android / Chrome）

## 项目内容
- `index.html`：完整 App 页面与功能
- `manifest.webmanifest`：PWA 安装配置
- `sw.js`：离线缓存
- `icon.svg`、`icon-192.png`、`icon-512.png`：桌面图标

## 最简单的免费部署方式：GitHub Pages
1. 在 Chrome 打开 https://github.com/ 并注册/登录。
2. 创建一个新仓库（Repository），名称填写 `photomind`，选择 Public。
3. 进入仓库，选择 Add file → Upload files。
4. 解压本压缩包，把里面四个文件上传到仓库根目录（不要只上传外层文件夹）。
5. 点击 Commit changes。
6. 进入仓库 Settings → Pages。
7. 在 Build and deployment 中选择 Deploy from a branch；Branch 选 `main`，文件夹选 `/ (root)`，保存。
8. 等待发布完成，打开 `https://你的用户名.github.io/photomind/`。
9. 在 Android Chrome 中打开网址，点右上角 ⋮ → 添加到主屏幕 / 安装应用。

## 使用
1. 点“导入照片”，从系统照片选择器多选照片。
2. 导入后可用搜索框查文件名、分类、标签和备注。
3. 点每张照片的“整理”添加分类、标签和备注。
4. 用日期框、分类框筛选。
5. 定期点“导出备份”，将 JSON 备份文件保存到安全位置。

## 隐私与限制
- 照片内容保存在当前 Chrome 网站的 IndexedDB 中；不会主动上传照片。
- GitHub Pages 只托管 App 程序文件，不接收你导入的照片。
- 第一版搜索的是文件名、分类、标签、备注；尚未实现图像内容 AI 识别和 OCR。
- 通过网页导入需要用户主动选择照片；不能在后台自动扫描整个 Android 相册。
- 不要清除 Chrome 的网站数据。清除网站数据、重置浏览器或更换设备可能造成本地照片库丢失。
- JSON 备份包含照片本身，可能很大；请妥善保管，避免公开分享。
- 当前按文件最后修改时间作为日期参考，不保证等于照片 EXIF 原始拍摄时间。
