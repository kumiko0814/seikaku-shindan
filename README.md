# Merone 性格診断

ソーシャルスタイル理論に基づく4タイプ（主導/促進/支持/分析）のコミュニケーションタイプ診断。
FAZOM社提供のGoogleフォーム版をMerone自社完結版として作り替えたもの。

- 診断: https://kumiko0814.github.io/seikaku-shindan/
- 管理: https://kumiko0814.github.io/seikaku-shindan/kanri.html （管理者ログイン方式・MeroneAdminAuth）

## 仕組み
- 20問・4件法。各タイプ5問×1〜4点＝5〜20点、最高点で判定（同点は併記）
- 結果保存: Supabase `promo_tasks` 相乗り（run_id=`seikaku-<ch>`、SQL作業ゼロ）
- 不具合報告: `ailab_notes` 相乗り（member_id=`bug_seikaku`）→ 管理ページ受信箱で対応済みトグル
- `?ch=xxx` でチャネル分離（例 `?ch=sales`）／ `?demo=1` 保存なし ／ `?debug=1` 画面内ログ ／ `?auto=1` 動作確認オートラン
