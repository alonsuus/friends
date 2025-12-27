# 友链管理仓库

本仓库用于管理 [Mininano](https://your-domain.com) 的友链。

## 申请友链

点击 [这里](https://github.com/alonsuus/friends/issues/new?labels=友链申请&template=friend-link.yml) 申请友链。

## 友链要求

- 站点内容健康，无违法违规信息
- 站点可以正常访问
- 建议提供RSS/Atom订阅地址

## 本站信息

- **站点名称**：Mininano
- **站点地址**：https://your-domain.com
- **站点描述**：个人博客 - 工作生活记录、折腾备忘
- **头像地址**：https://your-domain.com/avatar.webp
- **RSS地址**：https://your-domain.com/atom.xml

## 数据格式

```json
{
  "title": "站点名称",
  "url": "https://example.com",
  "screenshot": "https://example.com/avatar.png",
  "description": "一句话介绍",
  "feed": "https://example.com/atom.xml"
}
```

## 自动化

本仓库使用 GitHub Actions 自动化管理：

- ✅ 每天自动检查友链可达性
- ✅ 每天自动抓取最新文章（最多3篇）
- ✅ 自动生成友链数据文件

## 数据访问

友链数据：`https://raw.githubusercontent.com/alonsuus/friends/main/data.json`

## 管理说明

### 标签说明

- `友链申请` - 新申请（自动添加）
- `审核中` - 待审核（手动添加，不会显示在网站）
- `失联` - 无法访问（自动添加）
- `白名单` - 跳过检查（手动添加）

### 审核流程

1. 访客提交Issue
2. 管理员审核内容
3. 移除 `审核中` 标签（通过）或关闭Issue（拒绝）
4. 等待Actions自动更新（或手动触发）

### 手动触发更新

进入 **Actions** 标签，选择对应的Workflow，点击 **Run workflow**

## 技术栈

- [xaoxuu/issues2json](https://github.com/xaoxuu/issues2json) - Issue转JSON
- [xaoxuu/links-checker](https://github.com/xaoxuu/links-checker) - 友链检查器
- [xaoxuu/feed-posts-parser](https://github.com/xaoxuu/feed-posts-parser) - RSS解析器

---

**维护者**: [@alonsuus](https://github.com/alonsuus)
