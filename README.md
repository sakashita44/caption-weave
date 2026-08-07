# CaptionWeave

CaptionWeaveは、端末内で音声を文字起こしし、翻訳した原文と訳文をリアルタイムに表示するデスクトップアプリケーションである。マイクとシステム音声を入力として扱い、直前の発話と専門用語辞書を翻訳へ反映する。

実装計画と作業状況は[ロードマップIssue](https://github.com/sakashita44/caption-weave/issues/1)で管理する。

## 利用形態

音声認識は端末内で実行し、確定した文字列を翻訳APIへ送信する。配布物は、任意のディレクトリへ展開して実行するWindows向けportable ZIPである。

## ライセンス

CaptionWeaveの新規コードは[MIT License](LICENSE)で提供する。第三者のコード、ライブラリ、モデルには、それぞれのライセンスと利用条件が適用される。
