# Relatório de prontidão para lançamento - JurisBank

## Objetivo da rodada

Esta rodada buscou antecipar ajustes necessários para deixar o JurisBank mais próximo de uma versão lançável, sem tocar na planilha real e sem fazer push automático.

## Implementações realizadas

- Criada página pública `?p=avisos` para cadastro básico de interesse em Seletivos.
- Atualizado o botão `Receber avisos` do `index.html` para abrir `https://jurisbank.streamlit.app/?p=avisos`.
- Mantida a Área do Candidato livre do formulário de avisos, preservando a separação entre página pública, candidato e recrutador.
- Validada a sintaxe do `app.py` após as alterações.
- Conferida a presença de textos antigos/problemáticos no app e no index.

## Estado atual dos ambientes

### Público

- Entrada geral por `?p=publico`.
- Página de avisos por `?p=avisos`.
- Links do index apontam para candidato, recrutador e avisos.

### Candidato

- Menu logado: `Meu Perfil`, `Editar Perfil`, `Ver Seletivos`, `Sair`.
- Perfil do candidato mais limpo no topo.
- Login em formulário, permitindo envio por Enter.

### Recrutador

- Menu logado: `Perfil`, `Seletivos`, `Banco de Candidatos`, `Sair`.
- Perfil com atalhos para `Lançar Novo Seletivo` e `Meus Seletivos`.
- Criação de Seletivo com prazo em `dd/mm/aaaa`.
- Etapas selecionadas recebem prazo final próprio.

## Validações feitas

- `app.py` compilado com sucesso.
- `index.html` revisado quanto a acentuação corrompida.
- Confirmado que `Receber avisos` aponta para a nova página pública.
- Confirmado que não há ocorrência ativa de `date_input`, `+ Novo Seletivo` ou `Login para se inscrever`.

## Riscos antes do lançamento

- A página `?p=avisos` grava na aba de interesses. Isso é adequado para produção, mas exige que a aba exista e esteja acessível nas credenciais.
- A autenticação ainda é simples e baseada em sessão do Streamlit; para escala maior, será necessário reforçar autenticação e recuperação de senha.
- Fotos de perfil ainda dependem de armazenamento permanente para uso real consistente.
- O app segue concentrado em um único `app.py`; funciona, mas tende a ficar difícil de manter conforme crescer.
- É recomendável testar no Streamlit Cloud após deploy, com um usuário candidato e um usuário recrutador reais de teste.

## Próximos passos recomendados

1. Testar manualmente em produção:
   - cadastro/login candidato;
   - edição de perfil candidato;
   - inscrição em Seletivo;
   - login recrutador;
   - criação de Seletivo;
   - edição de Seletivo;
   - ver inscritos;
   - filtros do banco de candidatos.
2. Definir fluxo de recuperação de senha.
3. Definir política de armazenamento de fotos.
4. Criar uma rotina de backup/exportação da planilha.
5. Modularizar o app quando o fluxo estiver aprovado visualmente.
