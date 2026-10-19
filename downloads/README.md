# YLM統合版のダウンロード

## v0.5.1 Phase 1～4（2026-10-19）

[改良版ZIPをダウンロード（約7.6 MB）](https://github.com/timobi411/timobi/raw/refs/heads/master/downloads/ylm_scene_graph_integrated_v051_phase1_4.zip)

[GitHubのファイル画面](https://github.com/timobi411/timobi/blob/master/downloads/ylm_scene_graph_integrated_v051_phase1_4.zip) · [SHA-256](ylm_scene_graph_integrated_v051_phase1_4.zip.sha256)

v0.5.1-design-2に基づく複数仮説候補形成、証拠正規化・halo補完、beam探索、候補全体監査、独立したGT/代理事後評価、Viewerを追加しました。元v0.5 ZIPを変更せずvendorに保全しています。

26件の自動テスト、B0～B3・beam幅・最大断片数の9実行、Chromium画面操作を検証しました。日本語手順、schema、ソース、ログ、合成結果サンプルを同梱しています。展開後は `validation/sample_B3/index.html` でサンプルを閲覧できます。

正式v0.4結果は未受領のため、今回の結果は合成試験です。Phase 5の追加ICP初期化とPhase 6のScenarioはNOT_RUN、identityはUNKNOWN、updateはHELD、既存graph書込0です。実exp02の精度改善を確認したものではありません。

## v0.5 診断統合版（従来版）

[ZIPをダウンロード](https://github.com/timobi411/timobi/raw/refs/heads/master/downloads/ylm_scene_graph_integrated_v05_diagnostic.zip)

ZIPはPCに保存してから展開してください。GitHubのファイル画面からは「Download raw file」でも保存できます。

保存済みv0.4出力から構造監査・物体候補形成・旧ICP・幾何割当・更新案へ接続する診断版です。追加18件と元bridge3件の試験、および旧exp02実点群1組での元ICPとの数値一致を確認しました。

v0.4クラスタリング本体と正式結果が未受領のため、仕様書全体の完成版ではありません。物体同一性・更新精度は未評価で、既存シーングラフへの自動反映は行いません。詳しい実行方法・不足資料はZIP内のREADME_ja.mdとdocs/IMPLEMENTATION_STATUS.mdを参照してください。
