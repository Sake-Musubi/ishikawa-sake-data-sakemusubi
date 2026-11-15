# Changelog

版は `data/sake_ishikawa.json` の `version`（YYYY-MM-DD）と同じ。Release のタグは `v`＋版。
案内ページ（https://find-sake.me/open-data/）の「更新履歴」と同じ内容です。

## 2026-11-16

- 橋本酒造のお酒を、蔵の店頭（2026-11-15）と蔵元公式通販で確認し直しました（770→768本）。7本を追加し（大日盛 上撰、酒袋吊るししずく酒 吟彩金箔、純米酒 十代目 くらねこ酒、吟醸 雪古九谷、升々半升 十代目純米大吟醸原酒、熟成大吟醸 1992年醸造、熟成大吟醸 2002年醸造）、現行品として確認できなかった9本の掲載を終えました（十代目 しぼりたて生酒、十代目 本醸造、大日盛 普通酒 佳撰、真艫 本醸造 原酒、純米大吟醸 十代目 原酒 生詰、辛口 鐘馗 本醸造、酒袋吊るし 十代目 しぼりたて生酒、酒袋吊るし 純米生原酒 重右衛門、酒袋吊るし 醪のささやき）。
- 3本の名前を蔵の表記に合わせて改めました（「大吟醸 現代の名工」→「十年熟成大吟醸原酒 現代の名工」、「黄綬褒章受章 記念酒 大吟醸 前良平」→「十七年秘蔵酒 大吟醸原酒 黄綬褒章受章記念 前 良平」、「木槽 酒袋 しぼり 純米原酒 実盛」→「木槽酒袋しぼり 純米原酒 実盛」）。public_id と URL は変わりません。
- 同じ蔵の7本の値を、店頭の値札・裏ラベル・公式通販に合わせて直しました（原料米を「五百万石（国産）」「山田錦（国産）」に、容量・アルコール度数・日本酒度・酸度・火入れ／貯蔵・味わい7軸）。「純米吟醸 雪月花の舞」の日本酒度・酸度は、精米歩合が現行品と違う旧資料の値だったため null にしました。構造（schema）の変更なし。
- Re-checked Hashimoto Shuzo's sake against the brewery shop (2026-11-15) and its official online store (770 → 768). Added 7 sake (大日盛 上撰, 酒袋吊るししずく酒 吟彩金箔, 純米酒 十代目 くらねこ酒, 吟醸 雪古九谷, 升々半升 十代目純米大吟醸原酒, 熟成大吟醸 1992年醸造, 熟成大吟醸 2002年醸造) and delisted 9 that could not be confirmed as current products (十代目 しぼりたて生酒, 十代目 本醸造, 大日盛 普通酒 佳撰, 真艫 本醸造 原酒, 純米大吟醸 十代目 原酒 生詰, 辛口 鐘馗 本醸造, 酒袋吊るし 十代目 しぼりたて生酒, 酒袋吊るし 純米生原酒 重右衛門, 酒袋吊るし 醪のささやき).
- Renamed 3 sake to match the brewery's own labelling (大吟醸 現代の名工 → 十年熟成大吟醸原酒 現代の名工; 黄綬褒章受章 記念酒 大吟醸 前良平 → 十七年秘蔵酒 大吟醸原酒 黄綬褒章受章記念 前 良平; 木槽 酒袋 しぼり 純米原酒 実盛 → 木槽酒袋しぼり 純米原酒 実盛). Their public_id and URL are unchanged.
- Corrected values for 7 sake from the same brewery to match shop price cards, back labels and the official store (rice now 五百万石（国産） / 山田錦（国産）, volumes, ABV, Sake Meter Value, acidity, pasteurization, and the 7 taste axes). For 純米吟醸 雪月花の舞, the Sake Meter Value and acidity came from an older source whose polishing ratio differs from the current product, so they are now null. No schema change.

## 2026-11-14

- お酒を9本追加しました（761→770本）。既存のお酒の値の変更はありません。構造（schema）の変更なし。
- Added 9 sake (761 → 770). No changes to existing sake. No schema change.

## 2026-10-16

- 1本の名前を表ラベル・区分と小売店の表記に合わせて改めました（「宗玄 そっ甦」→「宗玄 純米酒 甦」、name_kana「そうげん じゅんまいしゅ そっ」、name_romaji「Sogen Junmaishu So」）。public_id と URL は変わりません。本数は761本のまま。構造（schema）の変更なし。
- Renamed one sake to match its label category and retail listings (宗玄 そっ甦 → 宗玄 純米酒 甦; name_kana "そうげん じゅんまいしゅ そっ", name_romaji "Sogen Junmaishu So"). Its public_id and URL are unchanged. Still 761 sake. No schema change.

## 2026-10-13

- お酒を13本追加しました（748→761本）。
- 5本の値を訂正しました。「竹葉 百万石乃白 大吟醸 初しぼり」は2026年の裏ラベルに合わせて度数17→15度・生原酒→生酒（tags から genshu を外す）。「奥能登の白菊 のとのなつやすみ」の原料米を「五百万石64%、山田錦36%」に、「能登末廣 純米吟醸 輪」の原料米は根拠が確認できないため未記載（null）に。「手取川 大吟醸生酒 あらばしり」と「能登大慶 純米酒 powered by Tengumai」は店頭表示（2026-10-11）に合わせて日本酒度を訂正し、前者は香りのタイプ、後者は仕込み水系（製造所に合わせ白山・手取川水系）と味わい7軸も見直しました。構造（schema）の変更なし。
- Added 13 sake (748 → 761).
- Corrected values for 5 sake: 竹葉 百万石乃白 大吟醸 初しぼり now follows the 2026 back label (ABV 17 → 15, 生原酒 → 生酒; genshu removed from tags); the rice of 奥能登の白菊 のとのなつやすみ is now "五百万石64%、山田錦36%"; the rice of 能登末廣 純米吟醸 輪 is now null (not documented) because its source could not be confirmed; the sake meter values of 手取川 大吟醸生酒 あらばしり and 能登大慶 純米酒 powered by Tengumai were corrected to match the in-store display (2026-10-11), along with the aroma type of the former and the water source (now that of the actual brewery, Hakusan/Tedori River system) and seven taste axes of the latter. No schema change.

## 2026-10-06

- お酒を33本追加し、5本の名前を改め、同じ商品が2件に分かれていた1本（宗玄 大吟醸 → 宗玄 大吟醸 Samurai King）を統合しました（716→748本）。
- 原料米（rice）の書き方を「品種（産地・栽培条件）割合」に統一（例「山田錦（兵庫県三木市吉川町・特A地区産）100%」「麹米：山田錦（兵庫県産）／掛米：五百万石（石川県産）」）。蔵元の公式情報・ラベルで確かめられた産地を215本に追記し、小売店の情報にしか根拠が無かった産地は外しました（353本の値が変わっています）。お酒の名前のローマ字（name_romaji）の表記揺れ5本を、同じ銘柄の他のお酒に揃えました（例「Yoshidagura u」→「Yoshidagura-u」）。構造（schema）の変更なし。
- Added 33 sake, renamed 5, and merged one sake that had been listed twice (宗玄 大吟醸 into 宗玄 大吟醸 Samurai King) (716 → 748).
- Unified the rice field to the form "variety (origin; cultivation) share" (e.g. "山田錦（兵庫県三木市吉川町・特A地区産）100%", "麹米：山田錦（兵庫県産）／掛米：五百万石（石川県産）"). Added rice origins confirmed by the brewery's own information or labels to 215 sake, and removed origins supported only by retailers (353 values changed). Aligned the romanized name (name_romaji) of 5 sake with the rest of their brand (e.g. "Yoshidagura u" → "Yoshidagura-u"). No schema change.

## 2026-09-26

- お酒を6本追加（「shu re 特別純米」「天平 本醸造五年古酒 上撰」「天平 本醸造三年古酒 佳撰」「遊穂 純米吟醸 百万石乃白50」「遊穂 みどりのゆうほ 生酛純米生酒」「遊穂 生酛純米 玉栄 生酒」）。構造（schema）の変更なし。
- Added 6 sake (shu re Tokubetsu Junmai, Tenpyo Honjozo Gonen Koshu Josen, Tenpyo Honjozo Sannen Koshu Kasen, Yuho Junmai Ginjo Hyakumangoku-no-shiro 50, Yuho Midori-no-yuho Kimoto Junmai Namazake, Yuho Kimoto Junmai Tamasakae Namazake). No schema change.

## 2026-09-22

- 初版（schema 1.0.0）。掲載中の全お酒のスペック・味わい7軸・蔵元確認状態を公開（CC BY 4.0・申請不要）。
- JSON / CSV / JSON Schema / Data Package。軸名・5段階の言葉・分類コード（特定名称・香りの質・酸のタイプ・製法/状態タグ）のラベルは8言語の言語マップ。範囲表記の元の範囲（ranges）、麹米・掛米の精米歩合（polishing_by_rice）、蔵元が意図して公開していない項目（undisclosed）を同梱。
- Initial release (schema 1.0.0): specifications, 7 taste axes and brewery-verification flags for all listed sake (CC BY 4.0, no registration).
- JSON / CSV / JSON Schema / Data Package. Axis names, level labels and code lists (designation, aroma type, acidity type, method/condition tags) as 8-language maps. Includes original ranges (ranges), per-rice polishing ratios (polishing_by_rice) and fields the brewery intentionally does not disclose (undisclosed).

