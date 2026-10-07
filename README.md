# CaptionWeave

CaptionWeaveは、端末内で音声を文字起こしし、翻訳した原文と訳文をリアルタイムに表示するデスクトップアプリケーションである。マイクとシステム音声を入力として扱い、直前の発話と専門用語辞書を翻訳へ反映する。

CaptionWeaveは開発中であり、利用できる版はまだ公開していない。

## 利用形態

音声認識は端末内で実行し、確定した文字列を翻訳APIへ送信する。配布物は、任意のディレクトリへ展開して実行するWindows向けportable ZIPである。

## 開発環境

.NET SDKのバージョンは`global.json`で固定し、[mise](https://mise.jdx.dev/)で導入する。品質ゲートは[pre-commit](https://pre-commit.com/)で実行し、pre-commitの導入には[uv](https://docs.astral.sh/uv/)を用いる。

新しい開発端末では、miseとuvをPATHから実行できる状態で、リポジトリのルートで次のコマンドを実行する。

```bash
mise install
bash scripts/setup.sh
```

`scripts/setup.sh`を実行すると、コミット時とpush時に検査を実行するフックが導入される。

| タイミング | 検査                                                                 |
| ---------- | -------------------------------------------------------------------- |
| コミット時 | シークレット検出、Markdown・JSON・YAMLの整形とリント、C#の空白の整形 |
| push時     | `dotnet build`、`dotnet test`                                        |
| PR         | コミット時とpush時の全検査（Windowsランナー）                        |

## ライセンス

CaptionWeaveの新規コードは[MIT License](LICENSE)で提供する。第三者のコード、ライブラリ、モデルには、それぞれのライセンスと利用条件が適用される。
