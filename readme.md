# Yahoo!ニュース 政治記事コメントスクレイピングツール

## ※ 注意事項

このスクリプトは Yahoo! JAPANの利用規約を適切に察した上で、研究や個人利用の範囲で使用してください。公開サービスでの使用や大量のアクセスは禁止される場合があります。

---

## 概要

Yahoo! JAPANの「国内 > 政治」カテゴリに表示された記事のURLを自動で取得し、その各記事に続くコメントを取得、JSON形式で保存するツールです。

---

## 使用技術

* Python 3.x
* Selenium
* ChromeDriver
* JSON / datetime / time

---

## 活用シーン

* 政治意見の分析
* 小規模なSNS意見測定
* テーマ別のトピック分析

---

## 出力の例 (JSON)

```json
{
  "https://news.yahoo.co.jp/articles/xxxx": {
    "title": "首相、再選への機運」など",
    "url": "https://news.yahoo.co.jp/articles/xxxx",
    "comments": [
      "政治に期待できない",
      "速やかな対応を期望"
    ]
  },
  ...
}
```

---

## 使用方法

1. Pythonの安装 (Selenium)

```bash
pip install selenium
```

2. ChromeDriverを現在のChromeバージョンに合わせてダウンロード
3. `scraper.py` を実行

```bash
python scraper.py
```

---

## 抽出所

* [https://news.yahoo.co.jp/categories/domestic](https://news.yahoo.co.jp/categories/domestic)

  * 政治タブをクリック
  * 「もっと見る」ボタンを10回クリック
  * 記事URL + タイトルを取得
  * `/comments` のURLに移動してコメント取得

---

## 追加機能 (optional)

* CSV保存
* pandasで測定数や評価
* ときどきブロックボタンが表示されない場合は retry

---

## 質問があれば

他のサイトのスクレイピングも対応可能です。
ご求人に合わせて操作の簡素化も可能です。
