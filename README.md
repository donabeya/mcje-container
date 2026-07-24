# mcje-container

どな鯖のマイクラ実行環境v1

# 実行
### 1. セットアップ
- [ここ見てrcloneを設定](https://rclone.org/remote_setup/)
    - 設定ファイルを`config/rclone/`へコピー
- プロジェクトルートで必須ディレクトリ作成

```bash
mkdir -p backups minecraft-data
```

### 2. コンテナ立ち上げ
```bash
sudo docker compose up -d   # 一括起動
sudo docker compose down    # 終了
```

# 監視とコマンド
```bash
sudo docker compose logs --follow           # 全コンテナのログをリアルタイムで見る

sudo docker exec -i mc rcon-cli             # RCON立ち上げ

sudo docker exec backup backup now          # 今すぐバックアップ
```

# システム

## デプロイ環境
- [WIKI参照](https://github.com/donabeya/mcje-docs/wiki/WIP:-server)

## つりー🌲

```
.
├── backups/        バックアップファイルの一時置き場
├── config/         設定ファイル置き場
│   ├── grafana/    ダッシュボード、アラートの設定(反映はwebから)
│   ├── mod/        MOD設定ファイル
│   └── rclone/     rclone設定ファイル置き場
├── grafana/        grafanaのデータベース等
├── minecraft-data/ コンテナ起動時のサーバープログラムが置かれる場所
├── prometheus/     監視
├── release/        現在未使用
└── compose.yml     サーバーシステムそのものf
```

## 構成図
![構成図](/image/minecraft.svg)

# Contributor

- インフラ担当大臣: [donabe8898](https://github.com/donabe8898)

- Mod担当大臣: zyashin0319

- ユーモア担当大臣: noriben0141, sugardegu2(副大臣)
