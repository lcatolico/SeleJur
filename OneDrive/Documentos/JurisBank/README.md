# SeleJur MVP

Protótipo inicial do SeleJur, baseado no app Streamlit existente do IndicaJur e direcionado para validação do fluxo de Seletivo.

## Objetivo

Validar a jornada:

Recrutador cria Seletivo -> compartilha link -> candidato se inscreve -> recrutador analisa inscritos em dashboard.

## Arquivos principais

- `app.py`: protótipo Streamlit.
- `requirements.txt`: dependências Python.
- `plano_mvp_seletivo.md`: decisão de produto e plano geral.
- `escopo_mvp_selejur.md`: escopo fechado do MVP.
- `roadmap_desenvolvimento_selejur.md`: fases de desenvolvimento e próximos marcos.
- `deploy_streamlit_cloud.md`: guia para publicar o MVP online e validar por link.
- `.streamlit/secrets.example.toml`: modelo de segredos para configurar no Streamlit Cloud.
- `melhorias_revisao_tecnica.md`: correções aplicadas após revisão técnica e limitações restantes.

## Como rodar

1. Instale as dependências:

```powershell
pip install -r requirements.txt
```

2. Configure os segredos do Streamlit para Google Sheets e autenticação.

O app espera credenciais em `st.secrets`, incluindo:

- `gcp_service_account`
- `sheet_id`
- `auth.salt`

3. Rode o app:

```powershell
streamlit run app.py
```

## Como validar com terceiros

Para validar com recrutadores ou candidatos em outro computador, publique o app online. Use o guia:

```text
deploy_streamlit_cloud.md
```

## Observações

- O app ainda usa Google Sheets como banco de prototipação.
- A base futura recomendada é Supabase para login, banco e documentos.
- O DISC deve ser tratado apenas como indicador comportamental de apoio.
- A IA deve apoiar resumo, triagem e entrevista, sem decidir aprovação ou reprovação.
