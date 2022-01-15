# はてぶ管理用
- githubactionを使用したはてぶ管理参考
  - https://tanabebe.hatenablog.com/entry/2020/07/06/080000

# how to use
## 記事の取得
- `master`ブランチにおいて
  - `docker-compose run blogsync pull ${blogdomain}`

## 記事追加、編集の前提
- branchの変更(master branchからの変更が投稿の対象)
  - git checkout -b [記事名]

## 記事の追加には
- 以下のコマンドを実行
```
docker-compose run blogsync post --title=draft --draft ${blogdomain} < draft.md
```

## 編集には、
- 該当のファイル`entries/[ドメイン名]/entry/YYYY/MM/DD/HHmmss.md`を編集して、投稿するだけ
  - github actionsが動いて自動投稿

## 画像の追加には、
- はてなブログ上において、画像を投稿、記事へ追加(記事の差分がうまれる)
- `master`で、記事を取得する
- `master`を編集のブランチへ統合


