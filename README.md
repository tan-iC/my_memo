# 備忘録

## Linux コマンド

1. du -h
    - ディレクトリサイズ確認

1. jobs
    - `ctrl + z`で停止中のものを表示

1. fg
    - `jobs`のindexを指定して`ctrl + z`で停止中のものを再開

## ネットワーク

1. DNSサーバ
    1. 自動で微妙な場合、固定に変更してみる

1. wsl
    1. wsl内部のDNS関連の設定を調べる
        - <https://qiita.com/kkato233/items/1fc71bde5a6d94f1b982>
    1. セキュリティソフトのファイアウォール設定を調べる・変更する
        - <https://kcm.trellix.com/corporate/index?page=content&id=KB94601>
        - ↑遅い
    1. プロキシを調べる
        - LAN、vpnの場合
