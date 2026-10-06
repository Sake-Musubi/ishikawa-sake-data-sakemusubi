# Changelog

版は `data/sake_ishikawa.json` の `version`（YYYY-MM-DD）と同じ。Release のタグは `v`＋版。
案内ページ（https://find-sake.me/open-data/）の「更新履歴」と同じ内容です。

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

