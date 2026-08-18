# SpatialScene Wallpaper

SpatialScene V3 空间壁纸公共仓库。本仓库保存用户投稿的原始图片，以及已经转换、
验证并可由 SpatialScene 使用的 `.spatialscene` 壁纸包。

## 目录结构

```text
Uploads/
  README.md               # 原始图片投稿入口与规则

Wallpapers/
  README.md               # 已发布壁纸说明
  <壁纸名称>.spatialscene/
    project.json
    assets/
    segmentation/         # 可选
```

- `Uploads/`：用于接收后续图片投稿。这里的图片不代表已经通过审核或已经生成
  空间壁纸。
- `Wallpapers/`：正式发布区，只保存经过转换和基本结构检查的
  `depth-field-v3` 壁纸包。

## 当前使用方式

目前可通过 Git clone 或 GitHub 下载仓库后，把 `Wallpapers/` 中需要的
`.spatialscene` 文件夹导入 SpatialScene。

```sh
git lfs install
git clone https://github.com/iyaway/SpatialSceneWallpaper.git
```

体积较大的 `.sstexture` 与 `.mov` 使用 Git LFS 保存；普通 clone 需要安装
Git LFS 才会自动取得实体内容。未来 App 将使用
`media.githubusercontent.com` 下载 LFS 实体，不会把 LFS pointer 当作壁纸。

SpatialScene App 后续将直接读取本仓库的壁纸索引并按需下载；该下载接口与
`index.json` 尚未在当前阶段启用。

## 壁纸命名

SpatialScene V3 的 iOS App、Mac App 与 Finder Quick Look 均以外部
`.spatialscene` 文件夹名作为显示名称，不读取或编辑内部
`project.json.name`。发布前请直接调整文件夹名。

## 投稿与发布

1. 原始图片放入 `Uploads/` 下独立的投稿目录。
2. 投稿者必须拥有图片版权或明确的再发布授权，并自行处理隐私与肖像权。
3. 维护者完成 PosterBoard/V3 转换、预览和结构检查后，才可移动到
   `Wallpapers/`。
4. 不接受符号链接、可执行文件或与壁纸无关的归档。
5. 未经审核的 Uploads 内容不会被未来 App 当作可下载壁纸。

## 格式边界

正式壁纸使用 SpatialScene 自有 `.ssmesh`、`.sstexture` 与公开 Metal
renderer。运行时不依赖 Apple 私有 renderer/framework，也不依赖本地 AI 模型。

---

This repository contains source-image submissions and published
`depth-field-v3` wallpaper packages for SpatialScene.
