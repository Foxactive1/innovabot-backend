# InNovaBot Backend

Este é o backend do **InNovaBot**, desenvolvido com **Flask** e pronto para ser implantado na nuvem com **Render**. Ele serve uma interface HTML, entrega músicas de forma dinâmica e responde a intents de um chatbot baseado em arquivos `.json`.

## Funcionalidades

- Servir interface HTML (`index.html`)
- Listar e recomendar faixas MP3 da pasta `/static/music`
- Gerar respostas de chatbot a partir de arquivos `.json` no diretório `arquivos_base`
- Autocomplete de sugestões de palavras
- Cache inteligente para evitar recomputação frequente

## Estrutura do Projeto

innovabot-backend/ ├── app.py ├── requirements.txt ├── render.yaml ├── arquivos_base/ │   └── list.json + arquivos JSON com intents ├── static/ │   └── music/ (faixas MP3) ├── templates/ │   └── index.html

## Deploy na Render

1. Suba este projeto para um repositório no GitHub
2. Acesse [https://render.com](https://render.com) e crie um serviço web
3. Configure com:
   - **Start Command:** `gunicorn app:app`
   - **Environment:** `Python`
   - **Root Directory:** `./`
4. Pronto! O InNovaBot estará acessível por URL pública

## Requisitos

- Python 3.8+
- Flask 2.2+
- Gunicorn (para produção)

Instalação local:

```bash
pip install -r requirements.txt
python app.py


---

InNovaBot é parte da iniciativa de inovação tecnológica da:

Dione Castro Alves
InNovaIdeia Assessoria em Tecnologia ®
LinkedIn | GitHub | innovaideia2023@gmail.com

