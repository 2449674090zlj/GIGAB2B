# GIGAB2B — 商品图片 CDN

Bed Frames 类目（LJ-Bed Frames 250-4）批量上传所需的商品图片，用于 Walmart 商品规格文件的图片直链。

## 用途

Walmart 要求图片 URL 满足：公网可访问、以图片扩展名结尾、不含查询参数。该仓库提供满足条件的静态直链。

## 目录结构

```
image/wkseller/<卖家ID>/<hash>.jpg
```

目录与文件名与原始图床对象路径完全一致，便于对照与替换。

## 直链格式

```
https://raw.githubusercontent.com/<用户名>/GIGAB2B/main/image/wkseller/<卖家ID>/<hash>.jpg
```

## 规格

- 格式：JPEG，RGB
- 尺寸：2200 × 2200（等比，部分原图为 2000 × 2000）
- 单张体积：≤ 1.58 MB（Walmart 限制 5 MB）
- 基准：Walmart 图片规范 5MB 以内、建议 2200×2200、1:1、白底

## 索引

`image-mapping.csv` 记录每个文件对应的 SKU、规格文件列号、原始 URL、压缩前后体积。

## 注意

本仓库需保持 **Public**，私有仓库的 raw 链接无法被 Walmart 抓取。
