# YLM統合版のダウンロード

## v0.5.1.2 接触境界・候補拡張監査（2026-10-21）

[改良版本体ZIPをダウンロード（約88.4 MB）](https://github.com/timobi411/timobi/raw/refs/heads/master/downloads/ylm_scene_graph_integrated_v0512_boundary_audit.zip)

[本体のファイル画面](https://github.com/timobi411/timobi/blob/master/downloads/ylm_scene_graph_integrated_v0512_boundary_audit.zip) · [本体SHA-256](ylm_scene_graph_integrated_v0512_boundary_audit.zip.sha256)

[E1～E4の詳細監査ログZIP（追加資料・約103.2 MB）](https://github.com/timobi411/timobi/raw/refs/heads/master/downloads/ylm_v0512_experiment_audit_logs.zip) · [ログSHA-256](ylm_v0512_experiment_audit_logs.zip.sha256)

design-2仕様に基づき、全画像接触のfloat64幾何、3D最近傍と画像距離の別端点参照、未保存親も再構成できる全拡張イベント、実際の保存選択履歴を追加しました。旧採否を保つE0/S0が既定で、S1保存とE1～E4探索は別の明示的な比較実験です。

4データ×5条件の全20実行で処理・監査が完了。E0では旧版と候補・保存順・画素ID・探索カウンタが一致し、保存候補は738／724／1,529／1,005件です。既存39件を変更せず新14件を加えた53テスト、全接触・イベント再照合、原本なし再生、Chromium操作を検証しました。

exp02 T1の全6,400生成イベントでは、all/eligible最短距離の差102件、eligible限定なら距離上限超過34件を確認しました。従来復元できた750件では差9件・超過0件で研究室報告と一致します。実際の判定は従来のall linksのままで、shadow結果を採否へ使いません。未保存53点候補は総枠到達により未訪問だったことも履歴で確認できます。

**まず本体を全体展開し、`ylm_scene_graph_integrated_v0512/validation/index.html` を開いてください。** 本体にソース・日本語手順・4ケースのE0完全出力・全条件比較・S0/S1結果を同梱しています。追加ZIPはE1～E4の完全な追加監査ログ・生成archiveで、元Viewer等を省いた記録集です。単独の再生用runではありません。

研究室のproxy_pixel_ids等は未受領のため、330画素の代理領域の再現評価は未実施です。探索網羅・物体精度の成功とは扱いません。identity=UNKNOWN、registration=NOT_RUN、update=HELD、既存graph書込0を維持します。

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
