# 🚀 GitHub Pages 部署指南

## 📋 前提条件

你已经有了：
- GitHub 用户名：`lxyyyyyy0917`
- GitHub Token：`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`
- 仓库名称：`what-eurekaliao-eat-today`

## 🎯 部署步骤

### 步骤 1：创建 GitHub 仓库

1. 访问 [GitHub](https://github.com)
2. 点击右上角的 `+` 号，选择 `New repository`
3. 仓库名称填写：`what-eurekaliao-eat-today`
4. 选择 `Public`（公开仓库才能使用免费的 GitHub Pages）
5. 不要勾选 "Initialize this repository with a README"
6. 点击 `Create repository`

### 步骤 2：上传代码到 GitHub

在你的项目文件夹中打开终端（命令行），执行以下命令：

```bash
# 初始化 Git 仓库
git init

# 添加所有文件
git add .

# 提交代码
git commit -m "Initial commit: 午餐选择助手"

# 添加远程仓库（使用你的 Token）
git remote add origin https://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@github.com/lxyyyyyy0917/what-eurekaliao-eat-today.git

# 推送到 GitHub
git push -u origin main
```

**注意**：如果提示分支名称是 `master` 而不是 `main`，请先执行：
```bash
git branch -M main
```

### 步骤 3：配置 GitHub Pages

1. 在 GitHub 仓库页面，点击 `Settings`（设置）
2. 在左侧菜单找到 `Pages`
3. 在 `Source` 部分：
   - 选择 `GitHub Actions` 作为部署源
4. 保存设置

### 步骤 4：等待自动部署

1. 返回仓库主页，点击 `Actions` 标签
2. 你会看到一个正在运行的工作流 `Deploy to GitHub Pages`
3. 等待几分钟，直到显示绿色的 ✓ 标记
4. 部署完成后，你的应用将在以下地址访问：

```
https://lxyyyyyy0917.github.io/what-eurekaliao-eat-today/
```

## 📱 添加到手机主屏幕

部署成功后，在手机上访问上述链接：

### iOS (Safari)：
1. 打开 Safari 浏览器访问你的应用
2. 点击底部的"分享"按钮（方框带向上箭头）
3. 向下滚动，找到"添加到主屏幕"
4. 点击"添加"
5. 应用图标会出现在主屏幕上

### Android (Chrome)：
1. 打开 Chrome 浏览器访问你的应用
2. 点击右上角的三个点菜单
3. 选择"添加到主屏幕"或"安装应用"
4. 点击"添加"
5. 应用图标会出现在主屏幕上

## 🔄 更新应用

当你需要更新应用时，只需：

```bash
# 修改代码后，提交更改
git add .
git commit -m "更新说明"
git push

# GitHub Actions 会自动重新部署
```

## 🛠️ 故障排除

### 问题 1：推送代码时提示权限错误
**解决方案**：确保使用了正确的 Token，命令格式为：
```bash
git remote set-url origin https://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@github.com/lxyyyyyy0917/what-eurekaliao-eat-today.git
```

### 问题 2：GitHub Actions 部署失败
**解决方案**：
1. 检查 Settings > Pages 是否选择了 `GitHub Actions`
2. 检查 Actions 标签页的错误日志
3. 确保仓库是 Public（公开）

### 问题 3：访问页面显示 404
**解决方案**：
1. 等待 5-10 分钟，GitHub Pages 需要时间生效
2. 确认访问的 URL 是：`https://lxyyyyyy0917.github.io/what-eurekaliao-eat-today/`
3. 清除浏览器缓存后重试

### 问题 4：Service Worker 缓存问题
**解决方案**：
如果更新后看不到新内容：
1. 在浏览器中按 `Ctrl + Shift + R`（Windows）或 `Cmd + Shift + R`（Mac）强制刷新
2. 或者清除浏览器缓存

## 📝 项目文件说明

- `index.html` - 主页面
- `app.js` - 应用逻辑
- `style.css` - 样式文件
- `manifest.json` - PWA 配置
- `sw.js` - Service Worker（离线支持）
- `.github/workflows/deploy.yml` - 自动部署配置

## 🎉 完成！

现在你的午餐选择助手已经部署到云端了！你可以：
- ✅ 在任何设备上访问
- ✅ 添加到手机主屏幕
- ✅ 离线使用
- ✅ 自动同步更新

享受你的可爱小助手吧！🍱💕