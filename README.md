# Kirimori AI

動画・静止画・スライドに、字幕と2D PNG／VRMキャラクターを重ねてMP4を作るWindows向け編集アプリです。AI台本、任意のAI読み上げ、別録り音声の文字起こしにも対応します。

このリポジトリは、Kirimori AIの公式リリース、更新情報、利用条件を案内するためのものです。アプリ本体のソースコード公開用リポジトリではありません。

## 配布ページ

- [BOOTH（無料版・任意の音声エンジンパック）](https://harako-ai.booth.pm/items/8701956)
- [GitHub Releases（公式リリース・更新ファイル）](https://github.com/kirimoriaisupport-gif/KirimoriAI-Releases/releases)

初めて導入する場合は、説明と必要ファイルをまとめて確認できるBOOTH版がおすすめです。GitHub Releasesでも同じ正式版を配布します。

## 主な機能

- 動画の時間トリミング、縦長・横長・正方形・フィード向け出力
- 動画、静止画、スライドを混在できるタイムライン
- 2D PNGアバターとVRMモデルの表示、表情、口パク、ポーズ
- 字幕の自動改行、サイズ・位置・デザイン調整
- LM StudioやGemini APIなどを使ったAI台本の下書き
- 任意導入のIrodori-TTS V4による読み上げ
- 任意導入のwhisper.cppによる別録り音声の文字起こし
- 高画質、SNS向け、Discord軽量版のMP4書き出し

AI機能を導入しなくても、手入力の字幕、動画内音声、2D PNG／VRM、画面デザイン、MP4書き出しを利用できます。

## 推奨動作環境

- OS: Windows 11 64bit
- CPU: Intel Core i5／AMD Ryzen 5相当以上、6コア以上推奨
- メモリ: 16GB以上推奨
- GPU: DirectX 11対応GPU
- ストレージ: 本体のみ2GB以上、TTS・STT・作業ファイル込みで20GB以上推奨
- 画面: 1920×1080以上推奨

Windows 10 22H2 64bitでも利用可能ですが、主な確認対象はWindows 11です。4K・60fps素材、長時間動画、多数のスライド、VRMの高画質出力では追加の性能と空き容量が必要です。

## インストール

1. Release assetsにある `Kirimori AI_*_x64-setup.exe` を実行します。
2. Windowsの案内に従ってインストールします。
3. 動画・静止画・スライドを読み込み、STEP 5からMP4を書き出します。

GitHubが自動表示する「Source code (zip)」はアプリのインストーラーではありません。

## 任意の音声エンジン

Release assetsでは、次の任意パックも配布します。

- `KirimoriAI-STT-whispercpp-ja-v1.9.1.zip`: 別録り音声の文字起こし
- `KirimoriAI-IrodoriTTS-Setup-v0.2.0.zip`: Irodori-TTS V4によるAI読み上げ

ZIPはすべて展開してから、同梱のセットアップを実行してください。導入と動作確認後は、ダウンロードしたZIP、展開したセットアップ用フォルダ、Kirimori AIのインストーラーを削除して構いません。

実際に使われるSTT/TTSは `%APPDATA%\KirimoriAI\engines` に保存されます。音声機能を利用中は、このフォルダを削除しないでください。

## AI台本

AI台本は任意機能です。右上の歯車から、OpenAI互換Chat Completions APIのURL、モデル名、必要な場合はAPIキーを入力します。

### LM Studioを使う場合

1. LM Studioで使用するモデルを読み込みます。
2. Developer画面のLocal Serverを開始します。
3. Kirimori AIへ次の値を入力します。

- Chat Completions URL: `http://127.0.0.1:1234/v1/chat/completions`
- モデル名: LM Studioに表示されるAPI Model Identifier
- APIキー: 通常は空欄

ポート番号を変更した場合は、URLの`1234`も同じ番号へ変更してください。

### Gemini APIを使う場合

- Chat Completions URL: `https://generativelanguage.googleapis.com/v1beta/openai/chat/completions`
- モデル名の例: `gemini-3.5-flash`
- APIキー: Google AI Studioで取得したキー

モデル名、利用上限、無料枠、URLは提供元の更新で変わる場合があります。利用時は各サービスの公式情報も確認してください。

外部APIを使用した場合、台本用の文章と最大8枚の代表フレームが指定した接続先へ送信されます。動画本体は送信しません。

## 利用条件とプライバシー

- [Kirimori AI 利用規約](LICENSE-ja.md)
- [プライバシー案内](PRIVACY-ja.md)
- [第三者ソフトウェア案内](THIRD_PARTY_NOTICES.md)

本アプリで作成した動画・画像は、商用・非商用を問わず利用できます。動画、画像、音声、VRM、キャラクターなど、利用者が追加する素材の権利は利用者自身で確認してください。

## 問い合わせ・不具合報告

- [問い合わせフォーム](https://docs.google.com/forms/d/e/1FAIpQLSflWWQjQvcG3Wx0x6J-n6tnIawcdU0VSOD1WFLpH25PtTU4UQ/viewform)
- サポートメール: kirimori.ai.support@gmail.com

不具合報告では、Kirimori AIのバージョン、Windowsのバージョン、行った操作、表示されたエラーを分かる範囲で記載してください。元素材、APIキー、個人情報を送る必要はありません。

## 更新について

正式公開版は更新情報のみを確認し、新しい版がある場合に配布ページを案内します。更新ファイルの自動ダウンロードや自動インストールは行いません。
