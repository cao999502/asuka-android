# 明日香AI - 安卓版（GitHub Actions 自动构建）

## 使用步骤（只需 3 步）

### 第 1 步：创建 GitHub 仓库
1. 访问 https://github.com/new
2. 仓库名称填 `asuka-android`（或其他名字）
3. 选择 **Public**（公开）或 **Private**（私有）都可以
4. 点击 **Create repository**

### 第 2 步：上传代码
在仓库页面，点击 **"uploading an existing file"**，然后把本项目所有文件拖进去：
- index.html
- package.json
- capacitor.config.json
- .github/workflows/build.yml

点击 **Commit changes**

### 第 3 步：等待构建完成
1. 点击顶部 **Actions** 标签
2. 你会看到名为 "Build Android APK" 的工作流正在运行
3. 等待约 3-5 分钟（第一次构建会下载依赖，较慢）
4. 构建完成后，点击进入该 workflow
5. 页面底部 **Artifacts** 区域会出现 `asuka-ai-apk`
6. 点击下载，解压后得到 `app-debug.apk`

## 更新应用

如果你修改了 `index.html`：
1. 在 GitHub 上编辑并提交修改
2. Actions 会自动重新构建
3. 下载新的 APK 即可

## 注意事项

- 构建的是 Debug APK，可以直接安装到任何安卓手机
- 如果 Actions 页面提示 "This workflow is not valid"，检查 `.github/workflows/build.yml` 格式是否正确
- 第一次构建可能需要 5-8 分钟，后续构建约 2-3 分钟
