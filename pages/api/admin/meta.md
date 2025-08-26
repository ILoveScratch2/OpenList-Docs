---
title:
  en: meta
  zh-CN: meta
icon: iconfont icon-token
# This control sidebar order
top: 140
# A page can have multiple categories
categories:
  - api
  - admin
# A page can have multiple tags
tag:
  - ADMIN
  - API
  - Guide
# this page is sticky in article list
sticky: true
# this page will appear in starred articles
star: true
---

## GET List Meta Info { lang="en" }

## GET 列出元信息 { lang="zh-CN" }

::: en
GET /api/admin/meta/list
:::
::: zh-CN
GET /api/admin/meta/list
:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| Name | Position | Type | Required | Description |
| ------------- | ------ | ------ | ---- | -------- |
| page | query | string | No | 页数 |
| per_page | query | string | No | 每页个数 |
| Authorization | header | string | Yes | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 说明 |
| ------------- | ------ | ------ | ---- | -------- |
| page | query | string | No | 页数 |
| per_page | query | string | No | 每页个数 |
| Authorization | header | string | Yes | none |
:::

### Response Example { lang="en" }

### 返回示例 { lang="zh-CN" }

::: en

> Success

```json
{
  "code": 200,
  "message": "success",
  "data": {
    "content": [
      {
        "id": 1,
        "path": "/a",
        "password": "i",
        "p_sub": false,
        "write": false,
        "w_sub": false,
        "hide": "",
        "h_sub": false,
        "readme": "",
        "r_sub": false
      }
    ],
    "total": 1
  }
}
```

:::
::: zh-CN

> 成功

```json
{
  "code": 200,
  "message": "success",
  "data": {
    "content": [
      {
        "id": 1,
        "path": "/a",
        "password": "i",
        "p_sub": false,
        "write": false,
        "w_sub": false,
        "hide": "",
        "h_sub": false,
        "readme": "",
        "r_sub": false
      }
    ],
    "total": 1
  }
}
```

:::

### Response Result { lang="en" }

### 返回结果 { lang="zh-CN" }

::: en
| Status Code | Status Code Meaning | Description | Data Model |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200 | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | 成功 | Inline |
:::
::: zh-CN
| 状态码 | 状态码含义 | 说明 | 数据模型 |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200 | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | 成功 | Inline |
:::

### Response Data Structure { lang="en" }

### 返回数据结构 { lang="zh-CN" }

::: en
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| ------------ | -------- | ----- | ---- | -------------------------- | ---- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | object | true | none | 数据 | none |
| »» content | [object] | true | none | 内容 | none |
| »»» id | integer | false | none | id | none |
| »»» path | string | false | none | 路径 | none |
| »»» password | string | false | none | 密码 | none |
| »»» p_sub | boolean | false | none | 密码是否应用到子文件夹 | none |
| »»» write | boolean | false | none | 是否允许写入 | none |
| »»» w_sub | boolean | false | none | 是否允许写入引用到子文件夹 | none |
| »»» hide | string | false | none | 隐藏 | none |
| »»» h_sub | boolean | false | none | 隐藏是否应用到子文件夹 | none |
| »»» readme | string | false | none | 说明 | none |
| »»» r_sub | boolean | false | none | 说明是否应用到子文件夹 | none |
| »» total | integer | true | none | 总数 | none |
:::
::: zh-CN
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| ------------ | -------- | ----- | ---- | -------------------------- | ---- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | object | true | none | 数据 | none |
| »» content | [object] | true | none | 内容 | none |
| »»» id | integer | false | none | id | none |
| »»» path | string | false | none | 路径 | none |
| »»» password | string | false | none | 密码 | none |
| »»» p_sub | boolean | false | none | 密码是否应用到子文件夹 | none |
| »»» write | boolean | false | none | 是否允许写入 | none |
| »»» w_sub | boolean | false | none | 是否允许写入引用到子文件夹 | none |
| »»» hide | string | false | none | 隐藏 | none |
| »»» h_sub | boolean | false | none | 隐藏是否应用到子文件夹 | none |
| »»» readme | string | false | none | 说明 | none |
| »»» r_sub | boolean | false | none | 说明是否应用到子文件夹 | none |
| »» total | integer | true | none | 总数 | none |
:::

## GET Get Meta Info { lang="en" }

## GET 获取元信息 { lang="zh-CN" }

::: en
GET /api/admin/meta/get
:::
::: zh-CN
GET /api/admin/meta/get
:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| Name | Position | Type | Required | Description |
| ------------- | ------ | ------ | ---- | -------- |
| id | query | string | Yes | 元信息id |
| Authorization | header | string | Yes | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 说明 |
| ------------- | ------ | ------ | ---- | -------- |
| id | query | string | Yes | 元信息id |
| Authorization | header | string | Yes | none |
:::

### Response Example { lang="en" }

### 返回示例 { lang="zh-CN" }

::: en

> Success

```json
{
  "code": 200,
  "message": "success",
  "data": {
    "id": 1,
    "path": "/a",
    "password": "c",
    "p_sub": false,
    "write": false,
    "w_sub": false,
    "hide": "",
    "h_sub": false,
    "readme": "",
    "r_sub": false
  }
}
```

:::
::: zh-CN

> 成功

```json
{
  "code": 200,
  "message": "success",
  "data": {
    "id": 1,
    "path": "/a",
    "password": "c",
    "p_sub": false,
    "write": false,
    "w_sub": false,
    "hide": "",
    "h_sub": false,
    "readme": "",
    "r_sub": false
  }
}
```

:::

### Response Result { lang="en" }

### 返回结果 { lang="zh-CN" }

::: en
| Status Code | Status Code Meaning | Description | Data Model |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200 | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | 成功 | Inline |
:::
::: zh-CN
| 状态码 | 状态码含义 | 说明 | 数据模型 |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200 | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | 成功 | Inline |
:::

### Response Data Structure { lang="en" }

### 返回数据结构 { lang="zh-CN" }

::: en
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| ----------- | ------- | ---- | ---- | -------------------------- | ---- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | object | true | none | | none |
| »» id | integer | true | none | id | none |
| »» path | string | true | none | 路径 | none |
| »» password | string | true | none | 密码 | none |
| »» p_sub | boolean | true | none | 密码是否应用到子文件夹 | none |
| »» write | boolean | true | none | 开启写入 | none |
| »» w_sub | boolean | true | none | 开启写入是否应用到子文件夹 | none |
| »» hide | string | true | none | 隐藏 | none |
| »» h_sub | boolean | true | none | 隐藏是否应用到子文件夹 | none |
| »» readme | string | true | none | 说明 | none |
| »» r_sub | boolean | true | none | 说明是否应用到子文件夹 | none |
:::
::: zh-CN
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| ----------- | ------- | ---- | ---- | -------------------------- | ---- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | object | true | none | | none |
| »» id | integer | true | none | id | none |
| »» path | string | true | none | 路径 | none |
| »» password | string | true | none | 密码 | none |
| »» p_sub | boolean | true | none | 密码是否应用到子文件夹 | none |
| »» write | boolean | true | none | 开启写入 | none |
| »» w_sub | boolean | true | none | 开启写入是否应用到子文件夹 | none |
| »» hide | string | true | none | 隐藏 | none |
| »» h_sub | boolean | true | none | 隐藏是否应用到子文件夹 | none |
| »» readme | string | true | none | 说明 | none |
| »» r_sub | boolean | true | none | 说明是否应用到子文件夹 | none |
:::

## POST Add Meta Info { lang="en" }

## POST 新增元信息 { lang="zh-CN" }

::: en
POST /api/admin/meta/create

> Body Request Parameters

```json
{
  "id": 0,
  "path": "/a",
  "password": "c",
  "p_sub": false,
  "write": false,
  "w_sub": false,
  "hide": "",
  "h_sub": false,
  "readme": "",
  "r_sub": false
}
```

:::
::: zh-CN
POST /api/admin/meta/create

> Body 请求参数

```json
{
  "id": 0,
  "path": "/a",
  "password": "c",
  "p_sub": false,
  "write": false,
  "w_sub": false,
  "hide": "",
  "h_sub": false,
  "readme": "",
  "r_sub": false
}
```

:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------- | ---- | -------------------------- | ---- |
| Authorization | header | string | Yes | | none |
| body | body | object | No | | none |
| » id | body | integer | Yes | id | none |
| » path | body | string | Yes | 路径 | none |
| » password | body | string | Yes | 密码 | none |
| » p_sub | body | boolean | Yes | 密码是否应用到子文件夹 | none |
| » write | body | boolean | Yes | 开启写入 | none |
| » w_sub | body | boolean | Yes | 开启写入是否应用到子文件夹 | none |
| » hide | body | string | Yes | 隐藏 | none |
| » h_sub | body | boolean | Yes | 隐藏是否应用到子文件夹 | none |
| » readme | body | string | Yes | 说明 | none |
| » r_sub | body | boolean | Yes | 说明是否应用到子文件夹 | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------- | ---- | -------------------------- | ---- |
| Authorization | header | string | Yes | | none |
| body | body | object | No | | none |
| » id | body | integer | Yes | id | none |
| » path | body | string | Yes | 路径 | none |
| » password | body | string | Yes | 密码 | none |
| » p_sub | body | boolean | Yes | 密码是否应用到子文件夹 | none |
| » write | body | boolean | Yes | 开启写入 | none |
| » w_sub | body | boolean | Yes | 开启写入是否应用到子文件夹 | none |
| » hide | body | string | Yes | 隐藏 | none |
| » h_sub | body | boolean | Yes | 隐藏是否应用到子文件夹 | none |
| » readme | body | string | Yes | 说明 | none |
| » r_sub | body | boolean | Yes | 说明是否应用到子文件夹 | none |
:::

### Response Example { lang="en" }

### 返回示例 { lang="zh-CN" }

::: en

> Success

```json
{
  "code": 200,
  "message": "success",
  "data": null
}
```

:::
::: zh-CN

> 成功

```json
{
  "code": 200,
  "message": "success",
  "data": null
}
```

:::

### Response Result { lang="en" }

### 返回结果 { lang="zh-CN" }

::: en
| Status Code | Status Code Meaning | Description | Data Model |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200 | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | 成功 | Inline |
:::
::: zh-CN
| 状态码 | 状态码含义 | 说明 | 数据模型 |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200 | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | 成功 | Inline |
:::

### Response Data Structure { lang="en" }

### 返回数据结构 { lang="zh-CN" }

::: en
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| --------- | ------- | ---- | ---- | ------ | ---- |
| » code | integer | true | none | | none |
| » message | string | true | none | | none |
| » data | null | true | none | | none |
:::
::: zh-CN
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| --------- | ------- | ---- | ---- | ------ | ---- |
| » code | integer | true | none | | none |
| » message | string | true | none | | none |
| » data | null | true | none | | none |
:::

## POST Update Meta Info { lang="en" }

## POST 更新元信息 { lang="zh-CN" }

::: en
POST /api/admin/meta/update

> Body Request Parameters

```json
{
  "id": 0,
  "path": "/a",
  "password": "c",
  "p_sub": false,
  "write": false,
  "w_sub": false,
  "hide": "",
  "h_sub": false,
  "readme": "",
  "r_sub": false
}
```

:::
::: zh-CN
POST /api/admin/meta/update

> Body 请求参数

```json
{
  "id": 0,
  "path": "/a",
  "password": "c",
  "p_sub": false,
  "write": false,
  "w_sub": false,
  "hide": "",
  "h_sub": false,
  "readme": "",
  "r_sub": false
}
```

:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------- | ---- | -------------------------- | ---- |
| Authorization | header | string | Yes | | none |
| body | body | object | No | | none |
| » id | body | integer | Yes | id | none |
| » path | body | string | Yes | 路径 | none |
| » password | body | string | Yes | 密码 | none |
| » p_sub | body | boolean | Yes | 密码是否应用到子文件夹 | none |
| » write | body | boolean | Yes | 开启写入 | none |
| » w_sub | body | boolean | Yes | 开启写入是否应用到子文件夹 | none |
| » hide | body | string | Yes | 隐藏 | none |
| » h_sub | body | boolean | Yes | 隐藏是否应用到子文件夹 | none |
| » readme | body | string | Yes | 说明 | none |
| » r_sub | body | boolean | Yes | 说明是否应用到子文件夹 | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------- | ---- | -------------------------- | ---- |
| Authorization | header | string | Yes | | none |
| body | body | object | No | | none |
| » id | body | integer | Yes | id | none |
| » path | body | string | Yes | 路径 | none |
| » password | body | string | Yes | 密码 | none |
| » p_sub | body | boolean | Yes | 密码是否应用到子文件夹 | none |
| » write | body | boolean | Yes | 开启写入 | none |
| » w_sub | body | boolean | Yes | 开启写入是否应用到子文件夹 | none |
| » hide | body | string | Yes | 隐藏 | none |
| » h_sub | body | boolean | Yes | 隐藏是否应用到子文件夹 | none |
| » readme | body | string | Yes | 说明 | none |
| » r_sub | body | boolean | Yes | 说明是否应用到子文件夹 | none |
:::

### Response Example { lang="en" }

### 返回示例 { lang="zh-CN" }

::: en

> Success

```json
{
  "code": 200,
  "message": "success",
  "data": null
}
```

:::
::: zh-CN

> 成功

```json
{
  "code": 200,
  "message": "success",
  "data": null
}
```

:::

### Response Result { lang="en" }

### 返回结果 { lang="zh-CN" }

::: en
| Status Code | Status Code Meaning | Description | Data Model |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200 | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | 成功 | Inline |
:::
::: zh-CN
| 状态码 | 状态码含义 | 说明 | 数据模型 |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200 | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | 成功 | Inline |
:::

### Response Data Structure { lang="en" }

### 返回数据结构 { lang="zh-CN" }

::: en
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| --------- | ------- | ---- | ---- | ------ | ---- |
| » code | integer | true | none | | none |
| » message | string | true | none | | none |
| » data | null | true | none | | none |
:::
::: zh-CN
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| --------- | ------- | ---- | ---- | ------ | ---- |
| » code | integer | true | none | | none |
| » message | string | true | none | | none |
| » data | null | true | none | | none |
:::

## POST Delete Meta Info { lang="en" }

## POST 删除元信息 { lang="zh-CN" }

::: en
POST /api/admin/meta/delete
:::
::: zh-CN
POST /api/admin/meta/delete
:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | ------ | ---- |
| id | query | string | Yes | | none |
| Authorization | header | string | Yes | | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | ------ | ---- |
| id | query | string | Yes | | none |
| Authorization | header | string | Yes | | none |
:::

### Response Example { lang="en" }

### 返回示例 { lang="zh-CN" }

::: en

> Success

```json
{
  "code": 200,
  "message": "success",
  "data": null
}
```

:::
::: zh-CN

> 成功

```json
{
  "code": 200,
  "message": "success",
  "data": null
}
```

:::

### Response Result { lang="en" }

### 返回结果 { lang="zh-CN" }

::: en
| Status Code | Status Code Meaning | Description | Data Model |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200 | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | 成功 | Inline |
:::
::: zh-CN
| 状态码 | 状态码含义 | 说明 | 数据模型 |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200 | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | 成功 | Inline |
:::

### Response Data Structure { lang="en" }

### 返回数据结构 { lang="zh-CN" }

::: en
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| --------- | ------- | ---- | ---- | ------ | ---- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | null | true | none | | none |
:::
::: zh-CN
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| --------- | ------- | ---- | ---- | ------ | ---- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | null | true | none | | none |
:::
