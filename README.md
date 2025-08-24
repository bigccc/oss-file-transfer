# 阿里云OSS文件中转站

一个功能强大的纯前端阿里云OSS文件管理工具，支持文件上传、管理、预览和分享。

![阿里云OSS文件中转站](https://img.shields.io/badge/阿里云-OSS文件中转站-blue)
![版本](https://img.shields.io/badge/版本-1.0.0-brightgreen)
![许可证](https://img.shields.io/badge/许可证-MIT-orange)

## 功能特点

### 基础功能
- ✅ 配置阿里云OSS账号信息
- ✅ 上传文件到OSS存储
- ✅ 管理已上传的文件（查看、复制链接、删除）
- ✅ 显示上传进度和状态通知

### 高级功能
- ✅ **文件夹管理**：创建、导航和删除文件夹
- ✅ **大文件分片上传**：自动分片上传大文件，支持断点续传
- ✅ **文件预览**：支持图片、视频、音频、PDF和文本文件的在线预览
- ✅ **批量操作**：支持批量上传和删除文件
- ✅ **文件搜索**：按名称搜索和按类型筛选文件
- ✅ **上传历史**：记录所有上传操作，包括成功、失败和取消的记录
- ✅ **文件有效期**：设置文件的有效期，过期后自动删除

## 快速开始

### 使用方法

1. 下载 `oss-file-transfer-enhanced.html` 文件
2. 在浏览器中打开该文件
3. 在"配置"页面填写您的阿里云OSS账号信息：
   - AccessKey ID
   - AccessKey Secret
   - Bucket名称
   - 地域（Region）
   - 自定义域名（可选）
4. 保存配置后即可开始使用

### OSS Bucket配置

为了确保应用正常工作，您需要正确配置OSS Bucket：

1. **跨域资源共享(CORS)设置**：
   ```
   来源(Origins): *（或您的网站域名）
   允许Methods: GET, POST, PUT, DELETE, HEAD
   允许Headers: *
   暴露Headers: ETag, Content-Length
   缓存时间(MaxAge): 600秒
   ```

2. **访问权限**：
   - 建议设置为"私有"以保证安全性
   - 如需公开访问，可设置为"公共读"

3. **RAM用户权限**：
   - 创建专用RAM用户并授予OSS相关权限
   - 使用RAM用户的AccessKey而非主账号

## 使用指南

### 文件上传

- 拖放文件到上传区域或点击选择文件
- 支持多文件同时上传
- 实时显示上传进度和速度
- 可随时取消上传任务

### 文件夹管理

- 点击"新建文件夹"创建文件夹
- 点击文件夹名称进入文件夹
- 使用面包屑导航返回上级目录
- 删除文件夹时会同时删除其中的所有文件

### 文件预览

- 支持图片缩放、旋转和全屏查看
- 支持视频和音频在线播放
- 支持PDF文档在线阅读
- 支持文本文件在线查看

### 批量操作

- 使用复选框选择多个文件
- 点击"全选"或"取消全选"
- 批量删除选中的文件

### 文件有效期

- 在配置页面设置默认文件有效期
- 支持永久有效、1天、7天、30天或自定义天数
- 过期文件会自动删除

## 技术栈

- **HTML5**：基础页面结构
- **Tailwind CSS**：样式设计
- **Font Awesome**：图标支持
- **阿里云OSS SDK**：OSS操作接口
- **原生JavaScript**：交互功能实现

## 安全性考虑

- AccessKey信息存储在浏览器的localStorage中
- 建议在生产环境中使用后端服务中转上传请求
- 或使用STS（Security Token Service）临时授权
- 定期轮换AccessKey增强安全性

## 许可证

MIT License

## 贡献指南

欢迎提交Issue和Pull Request来改进这个项目。

## 致谢

- [阿里云OSS](https://www.aliyun.com/product/oss)
- [Tailwind CSS](https://tailwindcss.com/)
- [Font Awesome](https://fontawesome.com/)