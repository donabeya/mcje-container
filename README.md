# mcje-container

サーバー実行環境

# 実行

## rcloneの設定
1. [https://rclone.org/remote_setup/](https://rclone.org/remote_setup/)


```bash
cd release/minecraft
sudo podman compose up -d
```

# リアルタイムで監視
```bash
# ログ
sudo podman compose logs --follow
# RCON
sudo podman exec -i testing-mc-1 rcon-cli
```

# システム

![構成図](/image/minecraft.svg)

```
release/testing
├── minecraft
│   ├── backups バックアップファイルの一時置き場
│   ├── config 設定ファイル置き場
│   │   ├── mod マイクラサーバーのMOD設定ファイル
│   │   └── rclone
│   ├── grafana
│   ├── minecraft-data コンテナ起動時のサーバープログラムが置かれる場所
│   ├── packwiz mod管理
│   ├── prometheus 監視
│   └── compose.yml サーバーシステムそのもの
└── garage *現在未使用
```

# Author

- donabe8898
