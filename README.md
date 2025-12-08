# mcje-container

どな鯖のマイクラ実行環境

# 実行
### 1. rcloneの設定
- リンク 👉 [https://rclone.org/remote_setup/](https://rclone.org/remote_setup/)

### 2. コンテナ立ち上げ
```bash
cd release/minecraft
sudo podman compose up -d
```

# 監視とコマンド
```bash
# ログ
sudo podman compose logs --follow
# RCON
sudo podman exec -i testing-mc-1 rcon-cli
# 今すぐバックアップ
sudo docker exec buckup buckup now
```

# システム

## デプロイ環境
- WIKI参照 👉 [https://github.com/donabeya/mcje-docs/wiki/WIP:-server](https://github.com/donabeya/mcje-docs/wiki/WIP:-server)

## つりー🌲
```
release/testing
├── minecraft
│   ├── backups バックアップファイルの一時置き場
│   ├── config 設定ファイル置き場
│   │   ├── grafana ダッシュボード、アラートの設定
│   │   ├── mod マイクラサーバーのMOD設定ファイル
│   │   └── rclone
│   ├── grafana
│   ├── minecraft-data コンテナ起動時のサーバープログラムが置かれる場所
│   ├── packwiz mod管理
│   ├── prometheus 監視
│   └── compose.yml サーバーシステムそのもの
└── garage *現在未使用
```

## 構成図
![構成図](/image/minecraft.svg)

# Contributor

- インフラ担当大臣: [donabe8898](https://github.com/donabe8898)

- Mod担当大臣: zyashin0319

- ユーモア担当大臣: noriben0141
