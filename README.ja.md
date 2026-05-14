# tsutsujibus-countdown

福井県鯖江市のコミュニティバス「つつじバス」向けのリアルタイム発車カウントダウンWebアプリケーションです。

ピンクを基調としたインターフェースで、ドロップダウンメニューから出発地と目的地を選択できます。次のバスまでのリアルタイムなカウントダウンとともに、直近5本の発車時刻をリスト表示します。

## デモ

**https://github.com/code4fukui/tsutsujibus-countdown

## 機能

- **リアルタイムカウントダウン**: 次の発車時刻までの分と秒を自動更新で表示します。
- **予定時刻一覧**: 選択したルートの直近5本の発車予定時刻をリスト表示します。
- **任意時刻検索**: 時刻入力フィールドを使用して、任意の時間帯の発車時刻を確認できます。
- **ルート交換**: ワンクリックで出発地と目的地を即座に入れ替えることができます。
- **共有リンク**: 選択したルートが自動的にURLへ反映されるため、簡単に共有できます。

## ローカルでの実行方法

1. **前提条件**: [Deno](https://deno.land/) がインストールされている必要があります。
2. **GTFSデータのダウンロード**: ターミナルで以下のコマンドを実行し、最新のバス時刻表データを取得します。
    ```bash
    deno run --allow-net --allow-write download.js
    ```
    これにより、プロジェクトディレクトリに必要な `gtfs_sabae.zip` ファイルがダウンロードされます。
3. **アプリの起動**: `index.html` ファイルをWebブラウザで開きます。

## データ・ライブラリ・クレジット

- **データソース**: [福井県オープンデータポータル](https://www.pref.fukui.lg.jp/doc/dx-suishin/opendata/gtfs_jp.html) より [鯖江市コミュニティバスつつじバス](https://www.pref.fukui.lg.jp/doc/dx-suishin/opendata/gtfs_jp_d/fil/gtfs_sabae.zip) のデータを取得しています。
- **コアライブラリ**: GTFS時刻表データの解析とクエリに [GTFS.js](https://github.com/code4fukui/GTFS) を使用しています。
- **フォーク元**: このプロジェクトは [発車カウントダウン - ハピラインふくい](https://code4fukui.github.io/hapiline-timetable/) をフォークしたものです。

## ライセンス

MIT License by Code for FUKUI
