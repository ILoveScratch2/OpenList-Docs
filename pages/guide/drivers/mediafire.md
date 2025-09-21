---
title:
  en: MediaFire
  zh-CN: Mediafire
icon: iconfont icon-state
# This control sidebar order
top: 520
# A page can have multiple categories
categories:
  - guide
  - drivers
---

::: en
Mount [MediaFire](https://www.mediafire.com/) cloud storage.

:::
::: zh-CN
挂载 [MediaFire](https://www.mediafire.com/) 云存储。

:::

## 根文件夹ID { lang="zh-CN" }

## Root folder path { lang="en" }

::: en
The default root directory for the path to mount mediafire, default is `/`.

:::
::: zh-CN
要挂载的Mediafire路径，默认为 `/`。

:::

## Session Token { lang="zh-CN" }

## Session Token { lang="en" }

::: en
Session Token

Open the browser developer tools, visit [mediafire.com](https://www.mediafire.com/), log in to your account, go to the `Network` tab, open `get_session_token.php`, find `session_token` in the `Response`, and copy its value to fill in.

![Mediafire Session Token](/img/drivers/mediafire/mediafire-sessiontoken.png)

:::
::: zh-CN
会话令牌

打开浏览器开发者工具，访问 [mediafire.com](https://www.mediafire.com/)，登录账号后，查看`Network`（网络）Tab，打开`get_session_token.php`，在`Response`（响应）中找到`session_token`，复制其值填入即可。

![Mediafire Session Token](/img/drivers/mediafire/mediafire-sessiontoken.png)

:::

## Cookie { lang="zh-CN" }

## Cookie { lang="en" }

::: en
Web Cookie

Open the browser developer tools, visit [mediafire.com](https://www.mediafire.com/), log in to your account, go to the `Network` tab, open `get_session_token.php`, find `Cookie` in the `Header`, and copy its value to fill in.

![Mediafire Cookie](/img/drivers/mediafire/mediafire-cookie.png)

:::
::: zh-CN
网页Cookie

打开浏览器开发者工具，访问 [mediafire.com](https://www.mediafire.com/)，登录账号后，查看`Network`（网络）Tab，打开`get_session_token.php`，在`Header`（标头）中找到`Cookie`，复制其值填入即可。

![Mediafire Cookie](/img/drivers/mediafire/mediafire-cookie.png)
:::
