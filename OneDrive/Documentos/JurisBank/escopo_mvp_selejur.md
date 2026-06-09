# Escopo Fechado do MVP - SeleJur

## Proposta

SeleJur e uma plataforma para recrutadores criarem Seletivos juridicos, compartilharem um link publico com candidatos e receberem uma triagem organizada com apoio de IA.

Frase curta:

> Crie um Seletivo juridico, receba candidatos por link e analise inscritos com resumos, filtros e recomendacoes assistidas por IA.

## Publico inicial

### Recrutador

Pessoa responsavel por selecionar candidatos para cargo em comissao, assessoria, gabinete, procuradoria, defensoria, ministerio publico, tribunal ou estrutura juridica publica/privada.

Necessidade principal:

- Reduzir tempo de triagem.
- Evitar curriculos soltos em e-mail ou WhatsApp.
- Comparar candidatos com mais clareza.
- Ter sugestoes de entrevista, prova ou periodo de experiencia.

### Candidato

Pessoa interessada no Seletivo, que recebe ou acessa um link, entende a oportunidade e se inscreve.

Necessidade principal:

- Entender a vaga.
- Enviar informacoes e curriculo facilmente.
- Responder perguntas relevantes.
- Confirmar inscricao sem friccao.

## Jornada do MVP

### 1. Recrutador cria conta

Campos minimos:

- Nome.
- E-mail.
- Senha.
- Orgao/instituicao.
- Cargo/função.
- Cidade/UF.

### 2. Recrutador cria Seletivo

Campos minimos:

- Titulo do Seletivo.
- Orgao/instituicao.
- Localidade.
- Modelo de trabalho.
- Prazo de inscricao.
- Descricao da oportunidade.
- Requisitos obrigatorios.
- Requisitos desejaveis.
- Perguntas para candidatos.
- Se deseja usar questionario comportamental de apoio.

Saida:

- Link publico unico do Seletivo.

### 3. Candidato acessa link

Pagina deve mostrar:

- Titulo.
- Orgao/instituicao.
- Localidade.
- Prazo.
- Descricao.
- Requisitos.
- Avisos importantes.
- Botao de inscricao.

### 4. Candidato se inscreve

Campos minimos:

- Nome.
- E-mail.
- Telefone.
- Cidade/UF.
- Formacao.
- Experiencia resumida.
- Curriculo em PDF.
- Respostas das perguntas do Seletivo.
- Questionario comportamental, quando habilitado.
- Consentimento de tratamento de dados.

### 5. Recrutador acompanha inscritos

Tela deve mostrar:

- Total de inscritos.
- Inscritos completos.
- Inscritos com pendencias.
- Lista de candidatos.
- Busca e filtros.
- Status da inscricao.

### 6. Recrutador analisa dashboard

Card de cada candidato:

- Nome.
- Formacao.
- Experiencia resumida.
- Status dos documentos/informacoes.
- Resumo do curriculo.
- Resumo das respostas.
- Aderencia aos requisitos.
- Perfil comportamental de apoio.
- Pontos fortes.
- Pontos de atencao.
- Perguntas sugeridas para entrevista.
- Sugestao de proxima etapa.

### 7. Recrutador solicita pre-entrevista em video

Depois da triagem inicial, o recrutador pode selecionar candidatos para uma fase de pre-entrevista em video.

Fluxo minimo:

- Recrutador seleciona candidatos no dashboard.
- Recrutador escolhe ou edita perguntas sugeridas.
- Sistema gera uma solicitacao de video para os candidatos selecionados.
- Candidato acessa a plataforma, grava ou envia video respondendo as perguntas.
- Recrutador assiste aos videos dentro do SeleJur.
- Recrutador registra anotacoes internas e decide a proxima etapa.

Uso recomendado:

- Confirmar comunicacao, postura e clareza de raciocinio.
- Reduzir entrevistas ao vivo desnecessarias.
- Preparar uma lista curta mais qualificada.
- Apoiar decisao sobre entrevista presencial, prova pratica ou periodo de experiencia.

Cuidados:

- Exigir consentimento especifico para envio e analise do video.
- Informar finalidade, prazo de armazenamento e quem tera acesso.
- Evitar uso automatico de IA para avaliar aparencia, voz, emocao ou caracteristicas sensiveis.
- Permitir que o recrutador avalie o conteudo da resposta, nao atributos pessoais protegidos.

## IA no MVP

### Entradas

- Descricao do Seletivo.
- Requisitos obrigatorios e desejaveis.
- Curriculo do candidato.
- Respostas do candidato.
- Resultado do questionario comportamental.

### Saidas

- Resumo executivo do candidato.
- Pontos de aderencia.
- Pontos de atencao.
- Perguntas sugeridas para entrevista.
- Sugestao de prova pratica ou periodo de experiencia, quando aplicavel.
- Perguntas sugeridas para pre-entrevista em video, quando o recrutador selecionar essa etapa.

### Limites

- A IA nao aprova nem reprova.
- A IA nao deve emitir laudo psicologico.
- A IA nao deve ocultar o criterio usado.
- O recrutador continua responsavel pela decisao.

## DISC no MVP

Nome sugerido no produto:

**Perfil comportamental de apoio**

Texto de aviso:

> Este perfil e um indicador comportamental simples para apoiar a entrevista. Ele nao substitui avaliacao tecnica, entrevista estruturada, analise curricular ou avaliacao psicologica formal.

Uso recomendado:

- Apoiar perguntas de entrevista.
- Ajudar o recrutador a observar estilo de trabalho.
- Complementar, nunca substituir, os demais criterios.

## Monetizacao inicial

### Gratuito ou basico

- Criar Seletivo simples.
- Receber inscricoes.
- Ver lista de candidatos.
- Ver dados enviados pelo candidato.

### Premium

- Resumo de curriculo por IA.
- Analise de aderencia.
- Perguntas de entrevista.
- Pre-entrevista em video.
- Armazenamento e painel de videos dos candidatos.
- Relatorio comparativo.
- Exportacao em PDF.
- Prova/teste customizado.
- Dashboard avancado.
- Comunicacao automatica com candidatos.

## Proxima implementacao no Streamlit

Prioridade imediata:

1. Ajustar marca e linguagem de IndicaJur para SeleJur nas telas de Seletivo. Status: iniciado.
2. Criar ou destacar pagina publica unica do Seletivo por link. Status: iniciado com parametro `sid` e link publico no painel do recrutador.
3. Simplificar inscricao do candidato para o fluxo do Seletivo. Status: iniciado com preservacao do Seletivo durante login/cadastro.
4. Melhorar dashboard do recrutador dentro de um Seletivo especifico. Status: iniciado.
5. Adicionar bloco de triagem assistida por IA, mesmo que inicialmente simulado/manual. Status: iniciado com triagem explicavel por regras.
6. Inserir aviso claro sobre IA e perfil comportamental. Status: iniciado.
7. Incluir pre-entrevista em video como fase pos-triagem. Status: iniciado com solicitacao, perguntas, prazo e candidatos convocados; upload direto depende de armazenamento proprio.

## Criterio de pronto

O MVP inicial esta pronto para validacao quando for possivel demonstrar, em uma unica jornada:

Recrutador cria Seletivo -> copia link -> candidato se inscreve -> recrutador abre dashboard -> recrutador entende rapidamente quem vale entrevistar e por que.
