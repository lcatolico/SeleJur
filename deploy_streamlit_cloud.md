# Publicacao Online - SeleJur no Streamlit Cloud

Este guia prepara a validacao externa do SeleJur por link.

## Objetivo

Permitir que recrutadores e candidatos testem o SeleJur pelo navegador, sem instalar nada.

## Arquivos necessarios

- `app.py`
- `requirements.txt`
- `.streamlit/config.toml`
- Secrets configurados no painel do Streamlit Cloud

Nao publicar credenciais reais no repositorio.

## 1. Preparar a planilha Google

Crie uma planilha Google com as abas usadas pelo app:

- `candidatos`
- `recrutadores`
- `chamadas`
- `interesses`
- `recomendacoes`
- `tokens`

Depois:

1. Copie os dados demo de `dados_demo/`.
2. Garanta que a primeira linha de cada aba tenha os cabecalhos.
3. Compartilhe a planilha com o e-mail da conta de servico do Google.
4. Copie o `sheet_id` da URL da planilha.

## 2. Criar conta de servico Google

No Google Cloud:

1. Crie ou selecione um projeto.
2. Ative Google Sheets API e Google Drive API.
3. Crie uma Service Account.
4. Gere uma chave JSON.
5. Use os campos do JSON no painel de secrets do Streamlit Cloud.

## 3. Configurar secrets no Streamlit Cloud

No app do Streamlit Cloud, abra:

`Settings -> Secrets`

Cole o conteudo baseado em:

`.streamlit/secrets.example.toml`

Preencha:

- `sheet_id`
- `sheet_name`
- `app.base_url`
- `[auth].salt`
- `[gcp_service_account]`
- `[resend]`, apenas se for testar envio de e-mail

## 4. Publicar

No Streamlit Cloud:

1. Conecte o repositorio.
2. Escolha branch principal.
3. Defina o arquivo principal como `app.py`.
4. Salve e aguarde o deploy.

## 5. Validar com terceiros

Enviar dois links:

### Recrutador demo

Link do app publicado.

Login:

- E-mail: `recrutador.demo@selejur.com`
- Senha: `demo123`

Tarefa:

- Entrar como recrutador.
- Abrir Meus Seletivos.
- Ver inscritos.
- Analisar triagem.
- Conferir pre-entrevista em video.

### Candidato

Enviar o link publico do Seletivo demo gerado no painel do recrutador.

Tarefa:

- Abrir o Seletivo.
- Entrar ou criar cadastro.
- Confirmar inscricao.
- Ver orientacoes caso convocado para video.

## 6. Feedback esperado

Perguntar ao validador:

- O fluxo fez sentido?
- Em que momento ficou confuso?
- O painel economizaria tempo?
- A triagem assistida ajudou ou atrapalhou?
- A pre-entrevista em video parece util?
- Que parte voce pagaria para usar?

## Cuidados

- Usar apenas dados ficticios na primeira demonstracao.
- Nao pedir documentos reais nesta fase.
- Nao usar videos reais sem consentimento explicito.
- Nao prometer decisao automatica por IA.
