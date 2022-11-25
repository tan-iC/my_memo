# 備忘録

## Environment

`pip freeze > requirements.txt`
`pip install -r requirements.txt`

## Git

1. .gitignore
    - 反映されないときは```git rm -r --cached .```
    - 一部ディレクトリの無視を回避`!/{$dir_name}`

1. ローカルからリモートの紐づけ
    - `git remote add origin {$remote_repo}`

1. push
    - 通らないときVPNとWSLの確認

## Linux command

1. du -h
    - ディレクトリサイズ確認

1. jobs
    - `ctrl + z`で停止中のものを表示

1. fg
    - `jobs`のindexを指定して`ctrl + z`で停止中のものを再開

1. bg
    - バックグラウンドで再開

1. screen
    1. 切れたとき
        1. `id`を`screen -ls`で調べる
        1. `kill {$id}`
        1. `kill`が効かなければscreen外から強制dettach`screen -d {$id}`

1. rsync
    - 空回し：`rsync -ahvn -e ssh {$src} {$dst} --exclude '*.pt' --exclude 'data/'`
    - 実行：`rsync -ahv -e ssh --progress {$src} {$dst} --exclude '*.pt' --exclude 'data/'`

## network

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

1. NAS
    1. 死んだらハードから再起動する
    1. httpsから接続して状況をモニターする
    1. 処理完了後はNASをマウントしているサーバ自体も再起動した方がよい（`sudo reboot`）
