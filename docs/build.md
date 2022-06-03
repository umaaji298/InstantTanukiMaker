# ビルド環境
- poetry (venv + vertualenvみたいなやつ)
https://cocoatomo.github.io/poetry-ja/basic-usage/

- 解説
https://zenn.dev/rihito/articles/1b096b1f695f06

## ビルド情報
pyproject.toml

## プロジェクト作成
poetry new my-package
または
poetry init

## 環境のセットアップ
poetry install

## 仮想環境へのアクセス
poetry shell

## 仮想環境から出る
exit

## パッケージ追加
poetry add <package-name>

# windows用実行ファイル作成
Nuitkaを利用(Cに変換して高速に動作するが初回ビルドは時間かかる)

- 公式
https://github.com/Nuitka/Nuitka

  - usecaseを順番に進めていくとビルドエラーを取り除いていけるかも

- 参考
https://blog.tsukumijima.net/article/python-nuitka-usage/

# モジュールのコンパイル
python -m nuitka --follow-imports program.py


## 配布用ビルド
python -m nuitka --standalone program.py

(対応版)
python -m nuitka --standalone --enable-plugin=numpy main.py

## 1ファイルパッケージ
python -m nuitka --onefile program.py

(対応版)
python -m nuitka --enable-plugin=numpy --onefile program.py

## データ梱包
python -m nuitka --enable-plugin=numpy --onefile --include-data-dir=Image=Image main.py

## アイコン追加
python -m nuitka --enable-plugin=numpy --onefile --include-data-dir=Image=Image --windows-icon-from-ico=Image\Icon\Instant.ico --windows-disable-console main.py

