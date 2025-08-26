---
title:
  en: auth
  zh-CN: auth
icon: iconfont icon-token
# This control sidebar order
top: 40
# A page can have multiple categories
categories:
  - api
# A page can have multiple tags
tag:
  - API
  - Guide
# this page is sticky in article list
sticky: true
# this page will appear in starred articles
star: true
---

## POST Get Token { lang="en" }

## POST token获取 { lang="zh-CN" }

::: en
POST /api/auth/login
Get temporary JWT token for a user, valid for 48 hours by default

> Body Request Parameters

```json
{
  "username": "{{alist_username}}",
  "password": "{{alist_password}}"
}
```

:::
::: zh-CN
POST /api/auth/login
获取某个用户的临时JWt token，有效期默认48小时

> Body 请求参数

```json
{
  "username": "{{alist_username}}",
  "password": "{{alist_password}}"
}
```

:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ---------- | ---- | ------ | ---- | ---------- | ---------- |
| body | body | object | No | | none |
| » username | body | string | Yes | 用户名 | 用户名 |
| » password | body | string | Yes | 密码 | 密码 |
| » otp_code | body | string | No | 二步验证码 | 二步验证码 |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ---------- | ---- | ------ | ---- | ---------- | ---------- |
| body | body | object | No | | none |
| » username | body | string | Yes | 用户名 | 用户名 |
| » password | body | string | Yes | 密码 | 密码 |
| » otp_code | body | string | No | 二步验证码 | 二步验证码 |
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
    "token": "abcd"
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
    "token": "abcd"
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
| --------- | ------- | ---- | ---- | ------ | ------ |
| » code | integer | true | none | | 状态码 |
| » message | string | true | none | | 信息 |
| » data | object | true | none | | data |
| »» token | string | true | none | | token |
:::
::: zh-CN
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| --------- | ------- | ---- | ---- | ------ | ------ |
| » code | integer | true | none | | 状态码 |
| » message | string | true | none | | 信息 |
| » data | object | true | none | | data |
| »» token | string | true | none | | token |
:::

## POST Get Token Hash { lang="en" }

## POST token获取hash { lang="zh-CN" }

::: en
POST /api/auth/login/hash
获取某个用户的临时JWt token，传入的密码需要在添加`-https://github.com/alist-org/alist`后缀后再进行sha256

> Body 请求参数

```json
{
  "username": "{{alist_username}}",
  "password": "{{alist_password}}"
}
```

:::
::: zh-CN
POST /api/auth/login/hash
获取某个用户的临时JWt token，传入的密码需要在添加`-https://github.com/alist-org/alist`后缀后再进行sha256

> Body 请求参数

```json
{
  "username": "{{alist_username}}",
  "password": "{{alist_password}}"
}
```

:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ---------- | ---- | ------ | ---- | ---------- | ----------------------------------------------------------------------- |
| body | body | object | No | | none |
| » username | body | string | Yes | 用户名 | 用户名 |
| » password | body | string | Yes | 密码 | hash后密码，获取方式为`sha256(密码-https://github.com/alist-org/alist)` |
| » otp_code | body | string | No | 二步验证码 | 二步验证码 |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ---------- | ---- | ------ | ---- | ---------- | ----------------------------------------------------------------------- |
| body | body | object | No | | none |
| » username | body | string | Yes | 用户名 | 用户名 |
| » password | body | string | Yes | 密码 | hash后密码，获取方式为`sha256(密码-https://github.com/alist-org/alist)` |
| » otp_code | body | string | No | 二步验证码 | 二步验证码 |
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
    "token": "abcd"
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
    "token": "abcd"
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
| --------- | ------- | ---- | ---- | ------ | ------ |
| » code | integer | true | none | | 状态码 |
| » message | string | true | none | | 信息 |
| » data | object | true | none | | data |
| »» token | string | true | none | | token |
:::
::: zh-CN
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| --------- | ------- | ---- | ---- | ------ | ------ |
| » code | integer | true | none | | 状态码 |
| » message | string | true | none | | 信息 |
| » data | object | true | none | | data |
| »» token | string | true | none | | token |
:::

## POST Generate 2FA Secret { lang="en" }

## POST 生成2FA密钥 { lang="zh-CN" }

::: en
POST /api/auth/2fa/generate
:::
::: zh-CN
POST /api/auth/2fa/generate
:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | ------ | ---- |
| Authorization | header | string | Yes | | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | ------ | ---- |
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
  "data": {
    "qr": "data:image/png;base64,iVBORw0KGgoAAAANSUhE",
    "secret": "RPQZG4MDS3"
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
    "qr": "data:image/png;base64,iVBORw0KGgoAAAANSUhE",
    "secret": "RPQZG4MDS3"
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
| --------- | ------- | ---- | ---- | ------ | -------------------- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | object | true | none | 数据 | none |
| »» qr | string | true | none | 二维码 | 二维码图片的data url |
| »» secret | string | true | none | 密钥 | none |
:::
::: zh-CN
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| --------- | ------- | ---- | ---- | ------ | -------------------- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | object | true | none | 数据 | none |
| »» qr | string | true | none | 二维码 | 二维码图片的data url |
| »» secret | string | true | none | 密钥 | none |
:::

## POST Verify 2FA Code { lang="en" }

## POST 验证2FA code { lang="zh-CN" }

::: en
POST /api/auth/2fa/verify

> Body Request Parameters

```json
{
  "code": "string",
  "secret": "string"
}
```

:::
::: zh-CN
POST /api/auth/2fa/verify

> Body 请求参数

```json
{
  "code": "string",
  "secret": "string"
}
```

:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | --------- | ---- |
| Authorization | header | string | Yes | | none |
| body | body | object | No | | none |
| » code | body | string | Yes | 2FA验证码 | none |
| » secret | body | string | Yes | 2FA密钥 | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | --------- | ---- |
| Authorization | header | string | Yes | | none |
| body | body | object | No | | none |
| » code | body | string | Yes | 2FA验证码 | none |
| » secret | body | string | Yes | 2FA密钥 | none |
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

## GET Get Current User Info { lang="en" }

## GET 获取当前用户信息 { lang="zh-CN" }

::: en
GET /api/me
:::
::: zh-CN
GET /api/me
:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | ------ | ---- |
| Authorization | header | string | No | | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | ------ | ---- |
| Authorization | header | string | No | | none |
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
    "username": "admin",
    "password": "",
    "base_path": "/",
    "role": 2,
    "disabled": false,
    "permission": 0,
    "sso_id": "",
    "otp": true
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
    "username": "admin",
    "password": "",
    "base_path": "/",
    "role": 2,
    "disabled": false,
    "permission": 0,
    "sso_id": "",
    "otp": true
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
| ------------- | ------- | ---- | ---- | ---------------- | ---- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | object | true | none | 数据 | none |
| »» id | integer | true | none | id | none |
| »» username | string | true | none | 用户名 | none |
| »» password | string | true | none | 密码 | none |
| »» base_path | string | true | none | 根目录 | none |
| »» role | integer | true | none | 角色 | none |
| »» disabled | boolean | true | none | 是否禁用 | none |
| »» permission | integer | true | none | 权限 | none |
| »» sso_id | string | true | none | sso id | none |
| »» otp | boolean | true | none | 是否开启二步验证 | none |
:::
::: zh-CN
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| ------------- | ------- | ---- | ---- | ---------------- | ---- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | object | true | none | 数据 | none |
| »» id | integer | true | none | id | none |
| »» username | string | true | none | 用户名 | none |
| »» password | string | true | none | 密码 | none |
| »» base_path | string | true | none | 根目录 | none |
| »» role | integer | true | none | 角色 | none |
| »» disabled | boolean | true | none | 是否禁用 | none |
| »» permission | integer | true | none | 权限 | none |
| »» sso_id | string | true | none | sso id | none |
| »» otp | boolean | true | none | 是否开启二步验证 | none |
:::

## GET List Current User SFTP Public Keys { lang="en" }

## GET 列出当前用户 SFTP 公钥 { lang="zh-CN" }

::: en
GET /api/me/sshkey/list
:::
::: zh-CN
GET /api/me/sshkey/list
:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | ------ | ---- |
| Authorization | header | string | Yes | | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | ------ | ---- |
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
  "data": {
    "content": [
      {
        "id": 1,
        "title": "Test-SSH-Key",
        "fingerprint": "SHA256:aAFI5C******************************KD6hYhs",
        "added_time": "2024-12-15T20:09:28.1777368+08:00",
        "last_used_time": "2024-12-15T20:10:07.7846528+08:00"
      },
      {
        "id": 2,
        "title": "Test-SSH-Key-2",
        "fingerprint": "SHA256:P2zrSs******************************h0Q5BOQ",
        "added_time": "2024-12-20T20:09:28.1777368+08:00",
        "last_used_time": "2024-12-25T20:10:07.7846528+08:00"
      }
    ],
    "total": 2
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
        "title": "Test-SSH-Key",
        "fingerprint": "SHA256:aAFI5C******************************KD6hYhs",
        "added_time": "2024-12-15T20:09:28.1777368+08:00",
        "last_used_time": "2024-12-15T20:10:07.7846528+08:00"
      },
      {
        "id": 2,
        "title": "Test-SSH-Key-2",
        "fingerprint": "SHA256:P2zrSs******************************h0Q5BOQ",
        "added_time": "2024-12-20T20:09:28.1777368+08:00",
        "last_used_time": "2024-12-25T20:10:07.7846528+08:00"
      }
    ],
    "total": 2
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
| ------------- | ------- | ---- | ---- | ---------------- | ---- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | object | true | none | 数据 | none |
| »» content | [object] | true | none | | none |
| »»» id | integer | true | none | 公钥主键 | none |
| »»» title | string | true | none | 公钥名称 | none |
| »»» fingerprint | string | true | none | 公钥指纹 | none |
| »»» added_time | string | true | none | 添加时间 | none |
| »»» last_used_time | string | true | none | 上次认证时间 | none |
| »» total | integer | true | none | 总数 | none |
:::
::: zh-CN
状态码 **200**
| 名称 | 类型 | 必选 | 约束 | 中文名 | 说明 |
| ------------------ | -------- | ---- | ---- | ------------ | ---- |
| » code | integer | true | none | 状态码 | none |
| » message | string | true | none | 信息 | none |
| » data | object | true | none | 数据 | none |
| »» content | [object] | true | none | | none |
| »»» id | integer | true | none | 公钥主键 | none |
| »»» title | string | true | none | 公钥名称 | none |
| »»» fingerprint | string | true | none | 公钥指纹 | none |
| »»» added_time | string | true | none | 添加时间 | none |
| »»» last_used_time | string | true | none | 上次认证时间 | none |
| »» total | integer | true | none | 总数 | none |
:::

## POST Add SFTP Public Key for Current User { lang="en" }

## POST 给当前用户添加 SFTP 公钥 { lang="zh-CN" }

::: en
POST /api/me/sshkey/add
:::
::: zh-CN
POST /api/me/sshkey/add
:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | ------ | ---- |
| Authorization | header | string | Yes | | none |
| body | body | object | No | | none |
| » title | body | string | Yes | 公钥名 | none |
| » key | body | string | Yes | 公钥内容 | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | -------- | ---- |
| Authorization | header | string | Yes | | none |
| body | body | object | No | | none |
| » title | body | string | Yes | 公钥名 | none |
| » key | body | string | Yes | 公钥内容 | none |
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
| ------------- | ------- | ---- | ---- | ---------------- | ---- |
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

## POST Delete Current User SFTP Public Key { lang="en" }

## POST 删除当前用户的 SFTP 公钥 { lang="zh-CN" }

::: en
POST /api/me/sshkey/delete
:::
::: zh-CN
POST /api/me/sshkey/delete
:::

### Request Parameters { lang="en" }

### 请求参数 { lang="zh-CN" }

::: en
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------ | ---- | ------ | ---- |
| Authorization | header | string | Yes | | none |
| id | query | integer | Yes | 公钥主键 | none |
:::
::: zh-CN
| 名称 | 位置 | 类型 | 必选 | 中文名 | 说明 |
| ------------- | ------ | ------- | ---- | -------- | ---- |
| Authorization | header | string | Yes | | none |
| id | query | integer | Yes | 公钥主键 | none |
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
| ------------- | ------- | ---- | ---- | ---------------- | ---- |
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
