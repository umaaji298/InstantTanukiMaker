# ビルド環境
- poetry (venv + vertualenvみたいなやつ)
https://cocoatomo.github.io/poetry-ja/basic-usage/

- 解説
https://zenn.dev/rihito/articles/1b096b1f695f06

# ビルド情報
pyproject.toml

# プロジェクト作成
poetry new my-package
または
poetry init

# 環境のセットアップ
poetry install

# 仮想環境へのアクセス
poetry shell

# 仮想環境から出る
exit

# パッケージ追加
poetry add <package-name>
