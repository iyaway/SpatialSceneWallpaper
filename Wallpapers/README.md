# Published Wallpapers

此目录是 SpatialScene 正式壁纸发布区。

每个壁纸必须是普通目录形式的 `<名称>.spatialscene` 包，并至少包含：

```text
<名称>.spatialscene/
  project.json
  assets/
    backfill.ssmesh
    backfill.sstexture
    main.ssmesh
    main.sstexture
```

`segmentation/` 为可选保留数据。壁纸显示名称直接取外部文件夹名。

`.sstexture` 与 `.mov` 通过 Git LFS 发布；`project.json`、`.ssmesh`、
`.plist` 和 `.heic` 保持普通 Git 文件。

未来 SpatialScene App 将使用仓库索引按需下载这里的壁纸；在索引启用前，
请通过 GitHub 或 Git clone 手动获取。
