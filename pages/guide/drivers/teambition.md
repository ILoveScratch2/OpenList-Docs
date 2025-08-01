---
title:
  en: Teambition
  zh-CN: Teambition
icon: iconfont icon-state
# This control sidebar order
top: 300
# A page can have multiple categories
categories:
  - guide
  - drivers
# A page can have multiple tags
tag:
  - Storage
  - Guide
  - '302'
# this page is sticky in article list
sticky: true
# this page will appear in starred articles
star: true
---

<!--@include: @/snippets/reverse-tip.md-->

::: en
Teambition project file, supports Chinese server and international server.
:::
::: zh-CN
Teambition 工程文件，支持中国服务器和国际服务器。
:::

## Cookies { lang="en" }

## Cookies { lang="zh-CN" }

::: en
After login, the validity period is unknown
![cookie](/img/drivers/teambition-cookie.png)
:::
::: zh-CN
登录后获取，有效期未知
![cookie](/img/drivers/teambition-cookie.png)
:::

## Project ID and root folder id { lang="en" }

## 项目 ID 和根文件夹 ID { lang="zh-CN" }

::: en
Get it from the URL after logging in
![id](/img/drivers/teambition-id.png)
:::
::: zh-CN
登录后从网址获取
![id](/img/drivers/teambition-id.png)
:::

## The default download method used { lang="en" }

# 默认使用的下载方式 { lang="zh-CN" }

::: en

```mermaid
---
title: Which download method is used by default?
---
flowchart TB
    style a1 fill:#bbf,stroke:#f66,stroke-width:2px,color:#fff
    style a2 fill:#ff7575,stroke:#333,stroke-width:4px
    subgraph ide1 [ ]
    a1
    end
    a1[302]:::someclass====|default|a2[user equipment]
    classDef someclass fill:#f96
    c1[local proxy]-.alternative.->a2[user equipment]
    b1[Download proxy URL]-.alternative.->a2[user equipment]
    click a1 "../drivers/common.html#webdav-policy"
    click b1 "../drivers/common.html#webdav-policy"
    click c1 "../drivers/common.html#webdav-policy"
```

:::
::: zh-CN

```mermaid
---
title: 默认使用的哪种下载方式？
---
flowchart TB
    style a1 fill:#bbf,stroke:#f66,stroke-width:2px,color:#fff
    style a2 fill:#ff7575,stroke:#333,stroke-width:4px
    subgraph ide1 [ ]
    a1
    end
    a1[302]:::someclass====|默认|a2[用户设备]
    classDef someclass fill:#f96
    c1[本机代理]-.备选.->a2[用户设备]
    b1[代理URL]-.备选.->a2[用户设备]
    click a1 "../drivers/common.html#webdav-策略"
    click b1 "../drivers/common.html#webdav-策略"
    click c1 "../drivers/common.html#webdav-策略"
```

:::
