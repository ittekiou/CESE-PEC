# 写し方 🐜

この箱は写してよい。写した箱は、そのまま一つの別荘（Commons）として動く。

## 1. 写す

[このテンプレートから写す](https://github.com/ittekiou/CESE-PEC/generate)。名前を決めて、**Public** で作る。`main` だけで足りる。

## 2. 札（`nest.json`）を書き換える

`name`・`url`（`/` で終える）・`about`・`lang`・`updated`・`feeds`・`links`・`nests`。

住所はふつう `https://あなた.github.io/箱の名前/`。札はそのうしろの `nest.json` に立つ。

`nests` に書くのは参照であって、所属ではない。

## 3. 会則（`README.md`）を書き換える

README は地図の上に会則として出る（`github.io` の住所のとき。独自ドメインでは札の `about` が出る）。会則は一条でよい。

## 4. `index.html` を見る

ページの題と説明（meta description）を自分のものに。ファビコンのパスに `CESE-PEC` と書いてあれば、自分の箱の名前に直すか、`favicon.png` のような相対パスにする。地図のしくみには触らなくてよい。

## 5. `feeds.json` を空にする（推奨）

```json
{
  "sll": "0.1",
  "commons": "https://あなた.github.io/箱の名前/",
  "collected_at": null,
  "nests": {}
}
```

最初の仕入れで丸ごと作り直されるので、しなくても困らない。前の別荘の便りが一時的に出るのを防ぐだけ。

## 6. 公開する

**Settings → Pages** で、Source を `Deploy from a branch`、Branch を `main`、Folder を `/ (root)`。

## 7. 仕入れを動かす

**Actions → Collect feeds → Run workflow**。緑になれば、あとは一日二回、勝手に仕入れる。書き込みの権限はワークフローが求めているので、ふつうは何もしなくてよい。

## 8. 見る

自分の住所を開いて、名前・会則・地図・便りが出ていれば、できあがり。

---

`scripts/collect.py` と `.github/workflows/collect.yml` は、そのままでよい。

ファイルを上げるときは「Add files via upload」のままにせず一行書くと、それが地図の便りになる。

あなたの箱も Template repository にすれば、また誰かが写せる。

**どっかでつながっとく。**
