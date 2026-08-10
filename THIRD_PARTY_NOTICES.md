# Kirimori AI 第三者ソフトウェア案内

更新日: 2026年8月9日

Kirimori AIには、HarakoAI以外の権利者が提供するソフトウェアが含まれます。各ソフトウェアには、それぞれのライセンスが適用されます。Kirimori AIの利用規約は、第三者ライセンスで認められた権利を制限しません。

## 動画処理

### FFmpeg 8.1.2 essentials build

- 配布元: https://www.gyan.dev/ffmpeg/builds/
- 対応ソース: https://github.com/FFmpeg/FFmpeg/commit/38b88335f9
- ライセンス: GNU General Public License version 3
- 利用方法: `ffmpeg.exe`と`ffprobe.exe`を独立したコマンドラインプログラムとして呼び出します。

完全なGPLv3本文は`LICENSE-FFmpeg-GPLv3.txt`、ビルド情報と入手先は`FFmpeg-SOURCE.txt`を確認してください。

## 3D表示

- three.js 0.185.1 — MIT License — https://github.com/mrdoob/three.js
- @pixiv/three-vrm 3.5.5 — MIT License — https://github.com/pixiv/three-vrm
- @pixiv/three-vrm-animation 3.5.5 — MIT License — https://github.com/pixiv/three-vrm

## デスクトップアプリ基盤・Rust依存

Kirimori AIはTauri 2とRustの依存crateを使用します。Windows x64公開版のロック済み実ビルド依存から生成した全277 cratesの版・宣言ライセンス・プロジェクトURLは`RUST-DEPENDENCIES.md`、収集したライセンス本文は`RUST-THIRD-PARTY-LICENSES.txt`に収録します。

生成元は次の開発用ファイルです。

- `docs/generated/rust-dependencies.md`
- `docs/generated/rust-license-texts.txt`
- `tools/generate-rust-license-inventory.mjs`

## 任意導入のAIエンジン

STT・TTSは本体とは別の任意パックです。各パック内の`THIRD_PARTY_NOTICES.md`とライセンスフォルダを確認してください。外部LLM API、LM Studio、利用者が追加したモデルや素材には、それぞれの提供元の利用条件が適用されます。

