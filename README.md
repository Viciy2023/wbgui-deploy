# wbgui-deploy

自动同步上游 [287775856/workbuddy2api-gui](https://github.com/287775856/workbuddy2api-gui)
并在 GitHub Actions 构建镜像推送至 GHCR。

- 镜像: `ghcr.io/viciy2023/wbgui-deploy:latest`
- 调度: 每 12 小时（UTC 00/12 = 北京 08/20）
- 上游无预构建镜像，本项目负责构建；Dockerfile 直用上游，无补丁
- `last-build.txt` 记录 `<上游SHA><BUILD_REV>` 指纹，改 `BUILD_REV` 可强制重建