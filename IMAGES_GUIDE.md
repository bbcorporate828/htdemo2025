# 图片部署指南 (Images Deployment Guide)

## 📁 文件结构

```
htdemo2025/
├── images/              ← 存放所有图片的文件夹
│   ├── sem-equipment.jpg
│   ├── hplc-equipment.jpg
│   ├── ftir-equipment.jpg
│   ├── lab-team.jpg
│   └── ...
├── index.html           ← 原始页面
├── index2.html          ← 新的 R&D Centre 页面
└── IMAGES_GUIDE.md      ← 本文件
```

---

## 🎯 从 Kossan 网站获取的关键图片

### **需要下载的图片**：

1. **SEM 设备图片** - Scanning Electron Microscopy
2. **HPLC 设备图片** - High-Performance Liquid Chromatography
3. **FTIR 设备图片** - Fourier Transform Infrared Spectrophotometer
4. **实验室团队照片**
5. **Contact Angle Tester**
6. **其他测试设备**

---

## 📥 方法 1: 手动下载图片（推荐用于 Demo）

### **步骤**：

1. **访问 Kossan 网站**：
   ```
   https://www.kossan.com.my/technology-innovation/index.html#cbp=ajax/rd-centre.html
   ```

2. **右键点击图片 → "另存为"**

3. **保存到本地 `images/` 文件夹**

4. **重命名为有意义的名称**：
   - `sem-equipment.jpg`
   - `hplc-equipment.jpg`
   - `ftir-equipment.jpg`
   - 等等

---

## 📥 方法 2: 使用免费占位图片（快速测试）

如果暂时没有真实图片，可以使用以下占位图服务：

### **Unsplash (高质量免费图片)**：
```html
<!-- 实验室设备 -->
<img src="https://images.unsplash.com/photo-1532187863486-abf9dbad1b69?w=800" alt="Laboratory Equipment">

<!-- 科学研究 -->
<img src="https://images.unsplash.com/photo-1582719471384-894fbb16e074?w=800" alt="Scientific Research">

<!-- 显微镜 -->
<img src="https://images.unsplash.com/photo-1530973428-5bf2db2e4d71?w=800" alt="Microscope">
```

### **Lorem Picsum (简单占位图)**：
```html
<img src="https://picsum.photos/800/600?random=1" alt="Placeholder">
```

---

## 🚀 部署图片到 GitHub Pages

### **步骤 1: 将图片放入 `images/` 文件夹**

```bash
# 在项目根目录
cd /Users/bwork/Documents/ht
```

将你的图片文件复制到 `images/` 文件夹中。

### **步骤 2: 添加到 Git**

```bash
git add images/
git commit -m "Add R&D equipment images"
git push origin main
```

### **步骤 3: 在 HTML 中引用**

```html
<!-- 本地图片引用 -->
<img src="images/sem-equipment.jpg" alt="SEM Equipment" class="w-full rounded-lg">
```

### **步骤 4: 访问线上图片**

部署后，图片 URL 为：
```
https://bbcorporate828.github.io/htdemo2025/images/sem-equipment.jpg
```

---

## 🎨 在 index2.html 中添加图片

### **示例：在 Page 3 添加设备图片**

找到对应的 `<div>` 标签，添加图片：

```html
<!-- SEM 卡片 -->
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition">
  <!-- 添加图片 -->
  <img src="images/sem-equipment.jpg" alt="SEM Equipment" class="w-full h-48 object-cover rounded-lg mb-4">
  
  <div class="w-20 h-20 bg-blue-100 rounded-full flex items-center justify-center mb-6 mx-auto">
    <!-- 图标代码 -->
  </div>
  <h3 class="text-xl font-bold mb-4 text-center">Scanning Electron Microscopy (SEM)</h3>
  <!-- 其他内容 -->
</div>
```

---

## 📋 推荐的图片规格

| 用途 | 尺寸 | 格式 | 文件大小 |
|------|------|------|----------|
| 设备照片 | 800x600px | JPG | < 200KB |
| 团队照片 | 1200x800px | JPG | < 300KB |
| 图标/Logo | 200x200px | PNG | < 50KB |
| 背景图 | 1920x1080px | JPG | < 500KB |

---

## 🔧 图片优化工具

### **在线压缩**：
- **TinyPNG**: https://tinypng.com/
- **Squoosh**: https://squoosh.app/

### **批量处理**：
```bash
# 使用 ImageMagick (需要安装)
mogrify -resize 800x600 -quality 85 images/*.jpg
```

---

## ✅ 快速部署清单

- [ ] 创建 `images/` 文件夹
- [ ] 下载/准备图片文件
- [ ] 优化图片大小（< 200KB）
- [ ] 重命名为有意义的文件名
- [ ] 运行 `git add images/`
- [ ] 运行 `git commit -m "Add images"`
- [ ] 运行 `git push origin main`
- [ ] 等待 GitHub Pages 部署（1-2分钟）
- [ ] 访问网站验证图片显示

---

## 🎯 当前状态

**已创建**：
- ✅ `images/` 文件夹（空）
- ✅ `index2.html`（使用 SVG 图标占位）
- ✅ 本指南文档

**待完成**：
- ⏳ 下载 Kossan 网站图片
- ⏳ 添加图片到 `images/` 文件夹
- ⏳ 更新 `index2.html` 引用图片
- ⏳ 推送到 GitHub

---

## 💡 提示

1. **图片命名规范**：使用小写字母和连字符，如 `sem-equipment.jpg`
2. **避免中文文件名**：可能导致部署问题
3. **使用相对路径**：`images/xxx.jpg` 而不是绝对路径
4. **测试本地**：在推送前先在本地浏览器测试

---

## 📞 需要帮助？

如果遇到问题，请告诉我：
- 图片无法显示
- 文件太大
- 需要修改图片位置
- 其他技术问题

