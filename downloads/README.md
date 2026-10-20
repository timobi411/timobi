# YLM統合版のダウンロード

## v0.5.1.1 候補探索改良（2026-10-20）

[改良版ZIPをダウンロード（約77.8 MB）](https://github.com/timobi411/timobi/raw/refs/heads/master/downloads/ylm_scene_graph_integrated_v0511_candidate_search.zip)

[GitHubのファイル画面](https://github.com/timobi411/timobi/blob/master/downloads/ylm_scene_graph_integrated_v0511_candidate_search.zip) · [SHA-256](ylm_scene_graph_integrated_v0511_candidate_search.zip.sha256)

画像4近傍の完全列挙と公平な幾何評価、Grid境界をまたぐ候補拡張、候補保存の多様性、段階別のペア監査Viewerを追加しました。v0.4入力と旧版ZIP、既存の幾何ゲートを保全しています。

正式exp01/exp02のT0/T1で24実行を比較。主条件5,000件の評価予算で、画像一意ペア978／941／2,190／1,206件の列挙・評価率100%を確認しました。C206–C245も評価・拡張試行に到達しています。保存多様性はデータ別に評価し、exp01 T0の最大集中率が旧版より高い点も報告しています。これらは探索指標であり、物体認識精度ではありません。

Ubuntu 22.04／Python 3.10で新版39試験・凍結旧版26試験が成功。原本のパスを参照できない環境での再生一致、ブラウザ操作、ZIP CRC・ファイルhashを検証しました。ソース、設定、入力アダプター、比較JSON、日本語報告、4データの完全なABC結果を同梱しています。

**ZIPをフォルダ全体で展開し、`ylm_scene_graph_integrated_v0511/validation/index.html` を開いてください。** 詳細な実行手順は `README_ja.md`、比較と制約は `validation/REPORT_ja.md` にあります。

GT精度・B2関係交換・exp08は未評価です。今回の仕様範囲に従いICP／割当／永続ID／更新は起動せず、registration=NOT_RUN、identity=UNKNOWN、update=HELD、既存graph書込0を維持します。

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
