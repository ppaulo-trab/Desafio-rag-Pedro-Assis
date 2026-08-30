# Desafio-rag-Pedro-Assis

# RAG - HTTPX

## Objetivo

Sistema de recuperação semântica baseado na documentação do HTTPX.

## Tecnologias

- Google Colab
- Python
- Sentence Transformers
- Transformers
- Gemma 3 1B

## Base documental

Repositório:
https://github.com/encode/httpx

Commit:
b5addb64f0161ff6bfe94c124ef76f6a1fba5254

Corpus:
httpx/docs/**/*.md

Quantidade:
23 arquivos

## Fluxo

documentos
→ chunks
→ embeddings
→ similaridade
→ top-k
→ Gemma 3

## Chunking

85 palavras
15 palavras de sobreposição

## Embeddings

sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2

## Recuperação

Similaridade por produto escalar entre embeddings normalizados.

## Geração

Gemma 3 1B Instruct.

A geração é opcional; a recuperação funciona independentemente dela.

## Testes

1. Pergunta claramente existente
2. Pergunta ampla
3. Pergunta fora do domínio

## Uso de IA

Ferramentas utilizadas:
- ChatGPT
- Gemma 3

A IA foi utilizada para para auxiliar no planejamento da arquitetura,
explicação de conceitos, geração inicial de trechos de código e
interpretação de erros.

Também foi utilizado o modelo Gemma 3 1B Instruct como componente
opcional de geração da resposta final.

Todo o código foi executado e validado no Google Colab, e as decisões
sobre chunking, embeddings, recuperação e tratamento de erros foram
testadas no contexto da documentação do HTTPX.
