# 石川県のお酒 味わいデータ（オープンデータ）／ Ishikawa Sake Taste Data (Open Data)

[酒結び（Sake-Musubi）](https://find-sake.me/) が石川県産の日本酒について独自に作成した、スペックと**味わい7軸**のデータです。
お酒ごとに、蔵元が内容を確認したかどうかの状態を付けています。

A dataset of sake from Ishikawa Prefecture, Japan, compiled independently by [Sake-Musubi](https://find-sake.me/): label specifications and a **7-axis taste profile** for each sake, with a per-sake flag showing whether the brewery has verified the content.

- **申請不要 / No registration required**
- **ライセンス / License: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)**（出典を書けば、商用・改変・再配布ができます / commercial use, modification and redistribution allowed with attribution）
- **最新版の固定URL / Latest version (stable URL):** https://find-sake.me/open-data/
- **過去の版 / Past versions:** この GitHub の [Releases](../../releases)

## ファイル / Files

| ファイル | 内容 |
| :---- | :---- |
| `data/sake_ishikawa.json` | 全件 JSON（UTF-8） |
| `data/sake_ishikawa.csv` | 全件 CSV（UTF-8 BOM 付き。Excel でそのまま開けます） |
| `data/sake_ishikawa.schema.json` | JSON Schema（draft 2020-12） |

```bash
curl -s https://find-sake.me/open-data/sake_ishikawa.json | jq '.record_count'
```

## できること・お願い / Terms

**できること / You may**

- ✅ 無料で使える / use it free of charge
- ✅ 商用・非商用を問わず使える / for commercial or non-commercial purposes
- ✅ 加工して使える / modify it
- ✅ 再配布できる（加工したものも） / redistribute it (including modified versions)

**ライセンスの条件は、出典を表示すること（下の「出典の書き方」）と、加工した場合はそれが分かるようにすること**の2つです（CC BY 4.0 第3条(a)(1)）。 / The license conditions are attribution (see below) and indicating any modification (§3(a)(1)).

**お願い / Requests**

- 酒結びがその利用を推奨・保証しているように見せないでください（CC BY 4.0 第2条(a)(6) の条件）。蔵元についても同様にお願いします（蔵元は確認者であって利用の当事者ではありません）。 / Do not imply endorsement by Sake-Musubi (§2(a)(6)) or by any brewery (a request).
- お酒や蔵の名前を事実として記載・引用することはできます。蔵の商品や公認サービスであるかのように見せる使い方（出所を示す標識としての使用）はライセンスの範囲外です（第2条(b)(2)。商標その他の権利は各蔵に帰属）。 / You may cite names as facts; using them as a mark of origin is outside the license (§2(b)(2)).
- `brewery_confirmed` の値にかかわらず「蔵元の公式値」と書かないでください。`true` は「蔵元が確認した」であって「蔵元が発表した値」ではありません。 / Do not describe the values as official brewery figures; `true` means reviewed, not published.
- 値を改変して再配布する場合は `brewery_confirmed` を `false` にするか列を落としてください。 / If you modify values and redistribute, set `brewery_confirmed` to `false` or drop the field.
- 加工した場合は原データと区別がつくようにしてください（第3条(a)(1)(B)）。 / Indicate modifications (§3(a)(1)(B)).

## 出しているもの／出していないもの / What is and isn't included

**出しているもの / Included**

- お酒の名前（日本語・かな・ローマ字）、酒結びのページURL / Sake name (Japanese, kana, romaji) and its page URL
- 蔵元名（日本語・ローマ字）、蔵の公式サイト / Brewery name and official website
- 特定名称、原料米、精米歩合、アルコール度数、日本酒度、酸度、使用酵母、仕込み水系、酒母・製法、搾り・濾過、火入れ・貯蔵、精米技術 / Designation, rice, polishing ratio, ABV, sake meter value, acidity, yeast, water source, starter method, pressing/filtration, pasteurization, milling technique
- 味わい7軸（各1〜5）、ガス感、香りの質、酸のタイプ / 7 taste axes (1–5), carbonation, aroma type, acidity type
- 存在する容量（ml） / Available bottle sizes (ml)
- 蔵元確認の状態（スペック／味わい）、情報の更新日 / Brewery-verification flags and the date of the information

**出していないもの / Not included**

- 商品画像は含まれていません。**酒結びのサイトに載っている画像も CC BY 4.0 の対象外です。**蔵元から酒結びに対して掲載の許諾を受けているもので、酒結びが第三者に使用を許可することはできません。使いたい場合は各蔵元へ直接（`brewery.website`）。ページへのリンク（`url`）は自由です。 / Product images are not included, **and the images on the Sake-Musubi site are not covered by this license either**: they are used with permission granted to Sake-Musubi, which cannot pass that permission on. Contact the brewery directly. Linking to the page (`url`) is fine.
- 商品説明の本文・おすすめの理由・7言語の訳文は含まれていません。蔵元が書いた文章や公式サイトを元にした文章を含むためです。 / Product descriptions, pairing notes and translations are not included; they contain text by or based on breweries.
- 取扱店・在庫・価格・店ごとの取扱容量は含まれていません。お店のデータであり、酒結びが公開を決められるものではないためです。 / Retailers, stock, prices and per-store bottle sizes are not included; that is the shops' data.
- 蔵元の連絡先は含まれていません。各蔵の公式サイト（`brewery.website`）からお願いします。 / Brewery contact details are not included; use `brewery.website`.
- アミノ酸度、共同醸造の第2蔵元、スペックの原文（範囲表記・「非公開」の別）はこの版に含まれていません（生成元の公開カタログが返さないため。次の版で検討）。 / Amino acidity, secondary breweries and original spec wording are not in this version.

## こんな使い方 / Example uses

- **お店の棚POP・飲食店のメニュー**：7軸をレーダーチャートにして貼る。「今日の魚に合う辛口」を `taste.sweet_dry >= 4` で絞る。 / Shelf tags and menus: radar charts of the 7 axes; filter dry sake with `taste.sweet_dry >= 4`.
- **アプリ・Webサービス**：好みの7軸ベクトルに近いお酒を並べる。`public_id` で酒結びのページへリンクすれば説明文・写真はそちらで見られます。 / Apps: rank sake by distance to a preference vector; link to Sake-Musubi via `public_id` for descriptions and photos.
- **研究・データ分析**：特定名称・原料米・精米歩合と味わい7軸の関係、蔵ごとの傾向。`brewery_confirmed` で蔵元確認済みの部分だけを取り出せます。 / Research: designation, rice, polishing ratio vs. taste; select verified records with `brewery_confirmed`.
- **多言語の下敷き**：かな・ローマ字・英語の軸ラベル（`axes[].levels_en`）が入っています。 / Multilingual listings: kana, romaji and English axis labels are included.

## 取得の仕様 / Format

| 項目 / Item | 内容 / Value |
| :---- | :---- |
| 固定URL / Stable URLs | `https://find-sake.me/open-data/sake_ishikawa.json` ・ `sake_ishikawa.csv` ・ `sake_ishikawa.schema.json`（常に最新版 / always the latest） |
| 言語 / Languages | 値は日本語（ラベル表記のまま）。名前にかな・ローマ字、蔵元名にローマ字を併記。キー名とスキーマは英語。7軸の軸名・5段階の言葉は8言語（日本語・英語・フランス語・イタリア語・ドイツ語・韓国語・繁体字・簡体字。`axes[].label_*` / `levels_*`）。商品説明の訳文は含まない / Values in Japanese as on the labels; kana and romaji for names; keys in English; axis names and level labels in 8 languages (ja, en, fr, it, de, ko, zh-TW, zh-CN) |
| 形式 / Encoding | JSON: UTF-8（BOM なし）。CSV: UTF-8 **BOM 付き**・CRLF・ヘッダ行あり / JSON: UTF-8 without BOM. CSV: UTF-8 with BOM, CRLF, header row |
| CSV の平坦化 / CSV flattening | 入れ子は `_` でつなぐ（`brewery_name`、`taste_sweet_dry`）。`volumes_ml` は `;` 区切り。真偽値は `true`/`false`、欠測は空欄 / Nested keys joined with `_`; `volumes_ml` separated by `;`; booleans `true`/`false`; missing values empty |
| CORS | `Access-Control-Allow-Origin: *` |
| キャッシュ / Cache | `Cache-Control: max-age=3600`。版は JSON 先頭の `version`（YYYY-MM-DD）と `source_commit` / Check `version` and `source_commit` at the top of the JSON |
| 認証・制限 / Auth, rate limit | なし。常識的な頻度で（1日1回で十分） / None. Please fetch at a reasonable rate |
| 過去の版 / Past versions | [Releases](../../releases)。タグは `v`＋版 / tagged `v` + version |

## データの構造 / Fields

フィールドの一覧と意味は https://find-sake.me/open-data/#fields、機械可読の定義は `data/sake_ishikawa.schema.json`（JSON Schema draft 2020-12）。
Field list: https://find-sake.me/open-data/#fields. Machine-readable definition: `data/sake_ishikawa.schema.json`.

## 蔵元確認フラグ / Verification flags

| 値 / Value | 意味 / Meaning |
| :---- | :---- |
| `brewery_confirmed.spec = true` | 数値スペックについて、酒結びの確認シートに蔵元から「この内容でよい」と回答があった。値は酒結びが整えたもので、蔵元の公式発表ではない / The brewery confirmed the specifications on Sake-Musubi's sheet; values are Sake-Musubi's, not an official publication |
| `brewery_confirmed.taste = true` | 味わい7軸についても同様の回答があった / The brewery likewise confirmed the 7 taste axes |
| `false` | 酒結びの独自調査値。蔵元は内容を保証していない / Independent research data by Sake-Musubi; not verified by the brewery |

確認を辞退した蔵と、まだお願いしていない蔵は区別せず、どちらも `false` です。`false` は蔵の意思の表明ではありません。`spec = true` かつ `taste = false` は「味わいについては回答がない・お願いしていない」場合を含みます。
Breweries that declined verification and those not yet asked are both `false`; `false` is not a statement of the brewery's position. `spec = true` with `taste = false` includes cases where the taste axes were not asked about or answered.

## 味わい7軸 / The 7 taste axes

全お酒を同じ物差しで比べるために酒結びが独自に算出した指標です。蔵元が公開している味わいの表現とは一致しないことがあります。**数値の大小は良し悪しではありません**（「飲みやすさ 1」＝「通好みの個性がある」）。1〜5 は順序尺度。
Custom metrics calculated by Sake-Musubi to compare all sake on one scale. They may differ from the brewery's own descriptions. **Higher is not better.** Ordinal 1–5.

| キー / Key | 軸 / Axis | 1 | 5 |
| :---- | :---- | :---- | :---- |
| `taste.sweet_dry` | 甘辛度 / Sweet / Dry | 大甘口 / Very sweet | 大辛口 / Very dry |
| `taste.acidity` | 酸味 / Acidity | 極めて穏やか / Very soft | 強い酸味 / Sharp |
| `taste.umami` | 旨味 / Umami | 極めてクリア / Very clean | 深いコク / Deeply savoury |
| `taste.aroma` | 香りの強さ / Aroma | 控えめ / Restrained | 極めて華やか / Highly fragrant |
| `taste.body` | ボディ・濃醇さ / Body | 超軽快 / Very light | 濃醇 / Rich |
| `taste.finish` | キレ / Crispness | 長い余韻 / Long finish | 極めて爽快 / Very crisp |
| `taste.drinkability` | 飲みやすさ / Drinkability | 通好みの個性 / For the initiated | スルスル飲める / Very easy |

2〜4 の文言は `data/sake_ishikawa.json` の `axes[].levels_ja` / `levels_en` にあります。
The wording for levels 2–4 is in `axes[].levels_ja` / `levels_en` in the JSON.

## データの作り方 / How the data was made

- **情報源 / Sources**：蔵元の公式サイト・オンラインショップ、裏ラベル・表ラベルの写真と店頭表示（2026年7月からの現地調査）、蔵元への確認シート（2026年8月〜。スペックと味わい7軸を別々に尋ね、`brewery_confirmed` に反映）。 / Breweries' official websites and shops; labels and shop displays photographed during field visits (from July 2026); a verification sheet sent to breweries (from August 2026).
- **処理 / Processing**：単位・符号を正規化。**範囲表記（例 16〜17度、+4〜+6）は中間値、「+4前後」は 4。麹米と掛米で異なる精米歩合は平均を丸めた値。**「非公開」「未記載」は `null`。味わい7軸は公開スペック・製法・味わいの記述から**酒結びが定めた基準**で1〜5に判定。生成AIに下書きさせ、1人が同じ基準で全件を確認・修正。提供温度は想定しない。 / Units and signs normalised; **ranges stored as the midpoint, differing koji/kake polishing ratios averaged**; "not disclosed"/"not stated" are `null`. Taste axes rated 1–5 by Sake-Musubi's own criteria; a generative model drafts, one person checks and corrects every record. No serving temperature is assumed.
- **蔵元確認 / Verification**：訂正を反映して確認済みの状態を付ける。管理画面・蔵元向けページから書き換えた場合は自動的に外れ、それ以外の経路は運用で外す。 / Corrections are applied and flagged; edits via the admin or brewery pages clear the flag automatically, other routes by procedure.
- **作り手 / Who**：酒結び（個人運営）。蔵元は情報源・確認者であって作成者ではない。個人情報は含まない。 / Sake-Musubi (an individual). No personal data.
- **もっと詳しく / More**：[7軸や数値の読み方（ガイド）](https://find-sake.me/sake-guide)。開発時の記録（参考。本数などは執筆時点）：[味を7つの数字にした](https://note.com/kazu5923k/n/n59847c4a53e9)（2026-09-06）／[銘柄では足りず626本を写経した夏](https://note.com/kazu5923k/n/nb6a464dd0e18)（2026-09-12） ／ English (machine-translated): [Converting taste into 7 numbers](https://note.com/kazu5923k/n/n59847c4a53e9?hl=en), [A summer of copying 626 bottles](https://note.com/kazu5923k/n/nb6a464dd0e18?hl=en)

## 限界と偏り / Limitations and bias

- 7軸は主観を含む推定値。蔵元確認済みは約1割。相対比較に使うこと。 / The taste axes are estimates; about a tenth are brewery-verified. Use for relative comparison.
- 県内の蔵はほぼ全蔵を収録しているが、蔵ごとの本数は 1〜70 本と偏る。酒販店で入手できたもの・公式サイトにあるものが中心で、限定品や小さな蔵のお酒は少ない。 / Almost every brewery is covered, but records per brewery range from 1 to 70; limited releases and small breweries are under-represented.
- 日本酒度・酸度は半数前後しか入っていない。欠測の大半は酒結びが情報源に値を見つけられなかったもので、蔵が意図して公開していないものは一部。欠測は無作為ではない。 / Sake meter value and acidity are present for only about half; most gaps are values not found in the sources, a smaller number are undisclosed by the brewery. Missingness is not random.
- 範囲表記は中間値、麹米・掛米で異なる精米歩合は平均値。測定値として引用しない。 / Ranges are midpoints and differing polishing ratios averages — do not cite as measurements.
- スペックは仕込みごとに変わる。`updated_at` はレコードの更新日で、採取日ではない（初回登録の基準日 2026-08-20 のままの本が多い。本数は案内ページの「この版の統計」に版ごとに出る）。 / Specifications change by batch; `updated_at` is the record's last-edited date, not the collection date.
- 各項目の記入率は https://find-sake.me/open-data/#stats に版ごとに出ている。 / Per-field fill rates for each version: https://find-sake.me/open-data/#stats

**推奨 / Recommendation**：数値スペックは蔵元の公式情報を正とし、このデータは索引に使う。7軸は「近い／遠い」の比較に使う。厳密さが要る用途では `brewery_confirmed = true` に絞る。

## 出典の書き方 / Attribution

データを使っている箇所か、それに近い場所（About・クレジット・注記）に、次のいずれかを載せてください。
Place one of the following at or near where the data is used (About, credits, footnote).

| 媒体 / Medium | 書き方 / Text |
| :---- | :---- |
| Web・アプリ / Web, app | `<a href="https://find-sake.me/open-data/">酒結び「石川県のお酒 味わいデータ（オープンデータ）」</a>（<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>）` |
| 印刷物・スライド・POP / Print, slides | `出典：酒結び「石川県のお酒 味わいデータ（オープンデータ）」（https://find-sake.me/open-data/）CC BY 4.0（https://creativecommons.org/licenses/by/4.0/）` |
| 論文・レポート / Papers | `酒結び「石川県のお酒 味わいデータ（オープンデータ）」版 YYYY-MM-DD, https://find-sake.me/open-data/, CC BY 4.0` |
| English | `Source: Sake-Musubi, "Ishikawa Sake Taste Data (Open Data)" (https://find-sake.me/open-data/), CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/)` |

加工した場合は「酒結びのデータを元に○○が加工」のように、原データと区別がつく書き方にしてください。
If you modified the data, say so (e.g. "based on data from Sake-Musubi, modified by ...").

BibTeX:

```bibtex
@misc{sakemusubi_ishikawa_sake_data,
  title   = {石川県のお酒 味わいデータ（オープンデータ） / Ishikawa Sake Taste Data (Open Data)},
  author  = {{酒結び / Sake-Musubi}},
  year    = {2026},
  version = {YYYY-MM-DD},
  url     = {https://find-sake.me/open-data/},
  note    = {CC BY 4.0}
}
```

## 使ったら教えてください（任意） / Tell us if you use it (optional)

[お問い合わせフォーム](https://find-sake.me/contact)（または [Issue](../../issues/new?template=used.md)）でサービス名と使った場所を教えていただけると、利用事例としてここに載せます。
プログラムから取得する場合は、URL の末尾に `?from=あなたのサービス名` を付けていただけると、どこで使われているかが分かって助かります（付けなくても取得できます）。

Tell us via the [contact form](https://find-sake.me/contact) (or an [issue](../../issues/new?template=used.md)) with your service name and where the data is used, and we will list it here. Appending `?from=your-service` to the download URL also helps us see where it is used (optional).

### 利用事例 / Used by

（まだありません / none yet）

## 更新・訂正・掲載終了 / Updates, corrections, delisting

- 更新は不定期で、予告なく最新版を公開します。利用者に個別にお知らせする仕組みはありません。世代の判定は JSON 先頭の `generated_at`（UTC）。 / Updated irregularly and without prior notice; there is no individual notification. Check `generated_at`.
- 訂正はサイトへ反映後、次の版に出します（不定期）。指摘いただいた項目だけを直し、確認済みは蔵元から回答があった軸にだけ付けます。 / Corrections appear in the next version (no fixed schedule); flags are set only for axes the brewery confirmed.
- 掲載終了は蔵元からのご依頼で次の版から外します。**CC BY 4.0 は撤回できない**（第2条(a)(1)）ので、既に配布した版と第三者の複製からは消せません。過去の Release から下げるかは個別に相談。サイトには載せたままオープンデータからだけ外すことにも応じます。 / Delisting takes effect from the next version. **CC BY 4.0 is irrevocable**: distributed versions and third-party copies cannot be recalled; removal from past releases is handled case by case. Removal from the open data only is also possible.
- 列の追加はあります。列の削除・意味の変更・キー名の変更も予告なく行うことがあり、何を変えたかは `CHANGELOG.md` に書きます。プログラムから使う場合は `generated_at` / `version` の変化を見て、取り込み前に構造を確かめてください。`public_id` は変えません。ライセンスは版ごとに固定で、後から狭めません。 / Columns may be added; removals and changes of meaning may also happen without notice and are recorded in `CHANGELOG.md`. Validate the structure before ingesting. `public_id` never changes. The license of a released version is never narrowed.

## ご注意 / Notes

- `null` は「情報源に記載がない」または「蔵元が公開していない」のどちらかです。日本酒度・酸度を意図して公開していない蔵があります。 / `null` means either "not stated by the source" or "intentionally not disclosed by the brewery".
- スペックは仕込みごとに変わります。値がいつ時点のものかは `updated_at` を見てください。 / Specifications vary from batch to batch; see `updated_at`.
- 掲載の有無や数値は、お酒の品質や優劣を示すものではありません。 / Nothing here ranks or judges the quality of any sake.
- 各レコードの値は `updated_at` 時点の情報です。蔵元確認は回答時点の内容に対するもので、確認日は載せていません。 / Each record is as of `updated_at`; verification refers to the content at the time of the reply.
- 内容の正確さ・完全さ・最新性・特定の目的への適合性を保証しません。利用によって生じた損害・不利益（誤った情報に基づく判断、事業上の損失、第三者との紛争を含む）について、法令上許容される範囲で酒結びは一切の責任を負いません（CC BY 4.0 第5条）。 / Provided as-is, without warranty; to the extent permitted by law Sake-Musubi accepts no liability for any loss or damage arising from use of this data (CC BY 4.0 §5).
- お酒の名前などを用いる際の第三者との権利関係は利用者の責任で処理してください。 / Clearing third-party rights in names you use is your responsibility.
- 個人が運営しており、更新の頻度や継続をお約束できません。 / Maintained by an individual; update frequency and continuity are not guaranteed.

## 連絡先 / Contact

- データについての問い合わせ・訂正の依頼（蔵元の方を含む）・利用のご報告 / Questions, corrections and usage reports: https://find-sake.me/contact
- [Issues](../../issues) も開いていますが確認の頻度は低いので、急ぎはフォームへ。 / Issues are open but checked less often; use the form for anything urgent.

## 更新のしかた（管理者向け） / Maintainer notes

データはアプリのビルド時に本番の公開カタログAPIから生成されます（`dev/frontend/tools/build-open-data.mjs`）。
このリポジトリは配信物のミラーで、**ここを手で直しても本番には反映されません**。

```bash
# アプリ側リポジトリで
cd 実装/dev/frontend && npm run build
python ../../scripts/export_open_data_repo.py <このリポジトリのクローン先>
# クローン先で commit → tag vYYYY-MM-DD → Release に data/ の3ファイルを添付
```

仕様の正は `実装/docs/仕様書/17_オープンデータ公開仕様.md`。
