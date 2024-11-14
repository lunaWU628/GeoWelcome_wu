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
...
  
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

或者一键部署到vercel——>[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/BDTA-zky/GeoWelcome)


### 说明：
1. **API 密钥配置**：你提到的 **申请 API 密钥**，需要在 API 提供商网站（例如 https://api.76.al/）注册并获取 API 密钥，并将其配置到项目中。为了更清楚地说明这一步，可以在 README 中添加具体的配置步骤。例如：
    ```markdown
    ## 配置 API 密钥

    1. 前往 [https://api.76.al/](https://api.76.al/) 注册并申请一个 API 密钥。
    2. 将获得的 API 密钥配置到项目中的 `CONFIG` 对象中：
    
    ```javascript
    const CONFIG = {
        API_KEY: '你的API密钥',
        ...
    };
    ```
    ```
