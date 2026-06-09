# Plano MVP - SeleJur

## Decisao de caminho

Vamos seguir pelo caminho hibrido:

- Usar o app Streamlit atual como base demonstravel e ambiente de validacao.
- Concentrar o MVP no fluxo de Seletivo.
- Manter o DISC apenas como apoio comportamental, sem promessa de avaliacao psicologica formal.
- Preparar a estrutura do produto para migracao futura para Supabase + app web + backend Python.

## Nome do produto

O nome recomendado para este produto e SeleJur.

Justificativa:

- Comunica diretamente selecao, seletivo e recrutamento juridico.
- E mais adequado ao fluxo de recrutadores criando Seletivos do que IndicaJur.
- Permite manter IndicaJur como produto, modulo ou conceito relacionado a indicacoes profissionais, se isso fizer sentido no futuro.
- Facilita explicar a proposta em uma frase: SeleJur e uma plataforma para criar Seletivos juridicos, receber candidatos e apoiar a triagem com IA.

## Objetivo do MVP

Permitir que um recrutador crie um Seletivo, compartilhe um link com candidatos, receba inscricoes estruturadas e visualize uma triagem assistida por IA para apoiar a decisao.

O MVP deve provar que:

- O recrutador consegue publicar um Seletivo com pouco esforco.
- O candidato consegue entender a oportunidade e se inscrever pelo link.
- O recrutador recebe as informacoes em formato melhor do que planilha, WhatsApp ou PDFs soltos.
- A IA economiza tempo ao resumir curriculos, respostas e pontos de atencao.

## Fluxo principal

1. Recrutador cria conta simples.
2. Recrutador cria um Seletivo.
3. Plataforma gera link publico do Seletivo.
4. Candidato acessa o link.
5. Candidato ve detalhes do Seletivo.
6. Candidato se cadastra ou confirma dados.
7. Candidato envia curriculo e informacoes complementares.
8. Candidato responde perguntas definidas pelo recrutador e questionario comportamental.
9. Prazo do Seletivo encerra.
10. Recrutador acessa dashboard com candidatos, resumos, pendencias, filtros e recomendacoes de entrevista.
11. Em fase posterior, recrutador pode solicitar pre-entrevista em video para candidatos selecionados na triagem.

## Paginas do MVP

### Recrutador

- Cadastro simples do recrutador.
- Login do recrutador.
- Painel inicial.
- Criacao de Seletivo.
- Lista de Seletivos publicados.
- Pagina de gestao de um Seletivo.
- Dashboard de inscritos.

### Candidato

- Pagina publica do Seletivo por link.
- Cadastro ou login simples.
- Formulario de inscricao.
- Upload de curriculo.
- Perguntas do Seletivo.
- Questionario comportamental de apoio.
- Tela de confirmacao da inscricao.

### Recrutador no Seletivo

- Lista de candidatos inscritos.
- Card resumido por candidato.
- Filtros por status, formacao, experiencia, documentos e aderencia.
- Resumo do curriculo.
- Resumo das respostas.
- Perfil comportamental de apoio.
- Pontos fortes.
- Pontos de atencao.
- Sugestoes de perguntas para entrevista.
- Sugestao de prova, entrevista ou periodo de experiencia quando aplicavel.

## IA no MVP

A IA deve atuar como assistente, nao como decisora.

Usos permitidos no MVP:

- Ler e resumir curriculo.
- Resumir respostas abertas.
- Identificar aderencias entre perfil e requisitos do Seletivo.
- Sugerir perguntas de entrevista.
- Sugerir prova pratica ou periodo de experiencia.
- Apontar pendencias documentais ou informacionais.

Usos que ficam fora do MVP:

- Aprovar ou reprovar candidato automaticamente.
- Prometer diagnostico psicologico.
- Fazer avaliacao DISC como laudo formal.
- Tomar decisao sem revisao humana.

## DISC como apoio comportamental

O DISC sera apresentado como indicador comportamental simples.

Regras:

- O resultado deve vir acompanhado de aviso claro.
- O texto deve dizer que o perfil e apenas apoio a entrevista.
- O recrutador deve ser estimulado a confirmar hipoteses em entrevista estruturada.
- O sistema nao deve usar DISC como criterio eliminatorio automatico.

## Monetizacao futura

Recursos basicos podem ser gratuitos ou de baixo custo:

- Criar Seletivo simples.
- Receber inscricoes.
- Ver lista basica de candidatos.

Recursos premium possiveis:

- Resumo de curriculo por IA.
- Triagem assistida.
- Ranking explicavel.
- Perguntas de entrevista sugeridas.
- Pre-entrevista em video para candidatos selecionados.
- Painel de videos com anotacoes do recrutador.
- Prova ou teste customizado.
- Relatorio comparativo.
- Exportacao em PDF ou planilha.
- Dashboard avancado.
- Comunicacao automatica com candidatos.

## Melhorias imediatas no Streamlit

Prioridade 1:

- Reorganizar o fluxo para que o Seletivo seja o centro do produto.
- Criar ou melhorar a pagina publica do Seletivo por link.
- Melhorar a experiencia de inscricao do candidato.
- Melhorar a pagina do recrutador no Seletivo.

Prioridade 2:

- Adicionar dashboard de triagem mais claro.
- Exibir cards comparaveis dos candidatos.
- Separar resumo, documentos, respostas, DISC e recomendacoes.
- Incluir avisos sobre uso da IA e do DISC.

Prioridade 3:

- Preparar dados para migracao futura.
- Mapear tabelas equivalentes no Supabase.
- Separar melhor regras de negocio, telas e armazenamento.

## Criterios de sucesso da validacao

O MVP sera considerado validado se, em testes com recrutadores reais ou simulados:

- O recrutador conseguir criar um Seletivo sem ajuda.
- O candidato conseguir se inscrever pelo link sem orientacao externa.
- O recrutador entender rapidamente quem sao os candidatos.
- O dashboard reduzir a necessidade de abrir curriculo por curriculo.
- As sugestoes de entrevista forem percebidas como uteis.
- O recrutador demonstrar disposicao a pagar por alguma camada premium.

## Proxima entrega recomendada

Transformar o codigo Streamlit atual em um MVP focado em Seletivo, removendo dispersoes do fluxo e criando uma primeira experiencia completa:

Recrutador cria Seletivo -> candidato se inscreve pelo link -> recrutador analisa inscritos em dashboard.
