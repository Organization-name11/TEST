# Pythonベースの開発環境
FROM mcr.microsoft.com/devcontainers/python:3.11

# ワークディレクトリをCodespacesの標準に合わせる
WORKDIR /workspace

# vcpkgなどの依存ツールがある場合はここでインストールしてもOK
# RUN git clone https://github.com/microsoft/vcpkg.git && ./vcpkg/bootstrap-vcpkg.sh

# Python依存のインストール
COPY requirements.txt /workspace/requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Flaskのポート設定
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_APP=server
