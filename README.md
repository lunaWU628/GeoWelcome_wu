# GeoWelcome
动态个性化欢迎页面，基于访客的地理位置和时间自动生成个性化的问候语。简单部署，一键发布，欢迎您的到来！

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/BDTA-zky/GeoWelcome)

GeoWelcome 是一个动态个性化欢迎页面，通过访问者的 IP 地址获取其地理位置，自动为其生成个性化的欢迎语、距离计算以及时间问候。你可以通过简单的配置和一键部署功能，将这个页面轻松地部署到 Vercel 或其他平台上，快速展示给访客。

## 功能
- **IP 地理位置识别**：通过访客的 IP 地址获取地理位置信息。
- **个性化欢迎语**：根据访问时间和位置，为每位访客定制不同的欢迎信息。
- **计算与博主的距离**：根据 IP 地址推算与博主的距离。
- **一键部署到 Vercel**：支持快速部署至 [Vercel](https://vercel.com/) 等平台。
- **响应式设计**：兼容各种设备，确保在手机、平板、电脑上都能完美显示。

## 特性
- 实时获取访客 IP 地址和地理位置。
- 基于不同时间段展示不同的问候语（如早上好、下午好等）。
- 支持博主自定义个人信息，如姓名、联系方式等。
- 支持通过 Vercel 一键部署，轻松上线。

## 部署到 Vercel

1. Fork 本仓库。
2. 登录 [Vercel](https://vercel.com/)。
3. 点击 **Import Project**。
4. 选择你 Fork 的仓库。
5. 点击 **Deploy** 按钮，Vercel 会为你提供一个访问链接。

或者一键部署到 Vercel ——> [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/BDTA-zky/GeoWelcome)

## 配置步骤

在将项目部署到 Vercel 之前，您需要修改一些基本配置，如 API 密钥、博主个人信息等。以下是如何修改配置文件的详细步骤。

### 1. 获取 API 密钥

GeoWelcome 使用外部服务获取访客的 IP 地址和地理位置。您需要在以下网站申请 API 密钥：

- 前往 [https://api.76.al/](https://api.76.al/) 注册并申请一个 API 密钥。
- 将获得的 API 密钥配置到项目的 `CONFIG` 对象中。

### 2. 配置 `CONFIG.js` 文件

在项目的根目录中找到 `index.html` 文件并打开。在文件中的 JavaScript 配置部分，您会看到一个名为 `CONFIG` 的对象。修改这个对象中的内容来配置您的 API 密钥、博主个人信息等。

```javascript
// 配置参数
const CONFIG = {
    BLOGGER_NAME: 'BUZZ', // 博主名字，请修改为您的名字
    EMAIL: 'mailto:2793217027@qq.com', // 博主的联系邮箱链接
    GITHUB_URL: 'https://github.com/BDTA-zky', // 博主的 GitHub 链接
    API_KEY: '4xR95RXijydgvLwXDmINz8ebaq', // API 密钥，请替换为您申请的 API 密钥
    BLOG_LOCATION: { lng: 113.506990, lat: 34.704587 }, // 博主的经纬度，修改为您的实际位置
    CACHE_DURATION: 1000 * 60 * 60, // 缓存时间，单位：毫秒（默认1小时）
    HOME_PAGE_ONLY: true, // 是否只在首页显示，设置为 true 只在主页显示
};
```
### 说明：

- **BLOGGER_NAME**：这里是博主的名字，您可以修改为您自己的名字或昵称。
- **EMAIL**：博主的联系邮箱链接。点击页面中的“发送邮件”时会自动打开邮件客户端。请将 `mailto:` 后面的邮箱地址替换为您的邮箱地址。
- **GITHUB_URL**：博主的 GitHub 链接。请将其替换为您的个人 GitHub 页面链接。
- **API_KEY**：您从 [https://api.76.al/](https://api.76.al/) 申请到的 API 密钥，请粘贴到这里。
- **BLOG_LOCATION**：博主的地理位置（经纬度）。您可以使用 [百度地图](https://map.baidu.com/) 或 [Google Maps](https://www.google.com/maps) 查找您的具体经纬度，填入 `lng`（经度）和 `lat`（纬度）。
- **CACHE_DURATION**：这是 API 数据的缓存时间，单位为毫秒。默认设置为 1 小时，您可以根据需要修改。
- **HOME_PAGE_ONLY**：如果您只希望在首页显示欢迎信息，设置为 `true`；如果希望在所有页面显示，设置为 `false`。

### 3. 本地测试

在修改好配置后，您可以在本地打开 `index.html` 文件查看效果。如果一切正常，您就可以部署到 Vercel 或其他平台了。

---

## 许可证

MIT © [BUZZ](https://github.com/BDTA-zky)
