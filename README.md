# mcje-container

サーバー実行環境

# 実行

```bash
cd ./testing
podman compose up -d
```

## RCON
```bash
sudo podman exec -i testing-mc-1 rcon-cli
> #ここでコマンド実行
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
