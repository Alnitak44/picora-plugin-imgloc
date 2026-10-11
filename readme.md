# ImgLoc 图床

为 Picora 添加 [ImgLoc](https://imgloc.com/) 图片上传支持。

## 使用

1. 在 Picora 1.0.1 或更新版本的插件中心导入 ZIP。
2. 在仓库中添加「ImgLoc 图床」配置，然后选择图片上传。

## 说明

1. 根据imgloc官方说明，你上传的图片只有一年储存期限过期会被删除，请注意不要用于长期使用的重要项目
2. 支持 JPG、PNG、GIF、WebP 四种常见格式，单张图片最大 10 MB。
3. 单个IP一小时内只允许上传最多60张照片。
4. 上传的照片不可管理不可删除，请注意不要传涉及隐私或其他不适宜公开的照片。
5. 请遵守图床规则和当地法律，勿滥用图床上传违法内容或用于违法用途，Picora不为之负责。

## 接口

- `GET /upload.php?action=token`：`ok`、`token`、`ttl`。
- `POST /upload.php`：multipart 字段 `image` 和 `token`；成功条件为 HTTP 200、`ok == true`，图片链接来自 `url`。

## 许可

[MIT](LICENSE)

> 这是第三方适配插件，不代表 ImgLoc 官方。
