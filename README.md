# private-rag-stack

完全オフライン・ローカルRAG環境

## 概要
Open WebUI + Ollama によるローカルRAGスタック。
外部APIへの通信は一切なし。機密情報・社内文書の検索に対応。

## 構成
| コンポーネント | 内容 |
|---|---|
| UI | Open WebUI |
| LLM | qwen3.5:9b（Ollama） |
| Embedding | nomic-embed-text（Ollama） |
| 外部通信 | **なし（完全オフライン）** |

## 前提条件
- Python 3.11+
- Ollama インストール済み

## セットアップ

\```bash
# Ollamaモデルのインストール
ollama pull qwen3.5:9b
ollama pull nomic-embed-text

# Open WebUI インストール・起動
pip install open-webui
open-webui serve
\```

ブラウザで http://localhost:8080 を開く

## 用途
- 機密情報を含む社内文書の検索
- 完全オフラインが必要な環境でのRAG
- セキュアなローカルAIチャット環境