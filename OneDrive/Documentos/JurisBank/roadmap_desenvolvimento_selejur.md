# Roadmap de Desenvolvimento - SeleJur

## Fase 1 - MVP de validacao

Objetivo: provar que o fluxo principal tem valor para recrutadores e candidatos.

### Entregas

- Recrutador cria conta.
- Recrutador cria Seletivo.
- Sistema gera link publico do Seletivo.
- Candidato acessa o link.
- Candidato cria cadastro ou entra na conta.
- Candidato envia informacoes profissionais e curriculo.
- Candidato responde perfil comportamental de apoio.
- Recrutador acompanha inscritos.
- Recrutador ve triagem assistida simples.
- Recrutador solicita pre-entrevista em video como fase posterior a triagem.

### Estado atual

- Base Streamlit criada em `app.py`.
- Marca SeleJur iniciada.
- Link publico por `sid` iniciado.
- Fluxo de retorno ao Seletivo apos login/cadastro iniciado.
- Dashboard de inscritos iniciado.
- Triagem assistida por regras iniciada.
- Solicitacao de pre-entrevista em video iniciada.
- Status por candidato no Seletivo iniciado.
- Upload real de video ainda pendente.

### Criterio de pronto

Uma demonstracao deve permitir:

Recrutador cria Seletivo -> copia link -> candidato se cadastra -> candidato se inscreve -> recrutador ve painel -> recrutador seleciona candidatos para video.

## Fase 2 - MVP comercial

Objetivo: transformar o prototipo em produto utilizavel por usuarios externos.

### Entregas

- Migrar login para Supabase Auth.
- Migrar dados de Google Sheets para Supabase Database.
- Migrar curriculos e documentos para Supabase Storage.
- Criar armazenamento proprio para videos.
- Separar candidato, recrutador, Seletivo, inscricao e etapas em tabelas proprias.
- Criar status por candidato dentro de cada Seletivo.
- Adicionar upload de documentos por Seletivo.
- Adicionar upload de video pelo candidato.
- Melhorar dashboard de triagem.
- Adicionar IA real para resumo de curriculo e respostas.

### Criterio de pronto

Um recrutador externo consegue conduzir um Seletivo real pequeno sem depender de planilha manual.

## Fase 3 - Monetizacao e premium

Objetivo: cobrar por recursos que economizam tempo e aumentam a qualidade da triagem.

### Entregas premium

- Resumo de curriculo por IA.
- Analise de aderencia com justificativa.
- Perguntas de entrevista sugeridas.
- Pre-entrevista em video.
- Relatorio comparativo entre candidatos.
- Exportacao em PDF ou planilha.
- Prova ou teste customizado.
- Comunicacao automatica com candidatos.
- Historico de Seletivos.

### Possiveis modelos de cobranca

- Por Seletivo publicado.
- Por pacote de candidatos analisados.
- Por modulo premium de IA.
- Por pre-entrevista em video.
- Assinatura mensal para recrutadores frequentes.

## Fase 4 - Produto robusto

Objetivo: preparar o SeleJur para escala, seguranca e operacao institucional.

### Entregas

- Permissoes por equipe.
- Logs de auditoria.
- Central de consentimentos.
- Politica de retencao de dados.
- Painel administrativo.
- Metricas de uso.
- Monitoramento de erros.
- Controle de custos de IA e armazenamento.
- Integração com e-mail e WhatsApp.
- Termos e politica de privacidade revisados juridicamente.

## Ordem recomendada agora

1. Fechar a Fase 1 no Streamlit.
2. Rodar uma demonstracao com dados simulados.
3. Ajustar a jornada com base no teste.
4. Validar com 2 ou 3 recrutadores.
5. Se houver sinal positivo, iniciar Fase 2 em Supabase.

## Proximo bloco de trabalho

Finalizar a Fase 1:

- Melhorar a tela publica do Seletivo.
- Tornar a inscricao do candidato mais direta.
- Criar uma visao de status por candidato no painel do recrutador. Status: iniciado.
- Sinalizar candidatos convocados para pre-entrevista em video. Status: iniciado.
- Preparar dados simulados para demonstracao. Status: iniciado com pacote `dados_demo`.
