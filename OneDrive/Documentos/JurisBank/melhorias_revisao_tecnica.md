# Melhorias aplicadas da revisao tecnica

## Corrigido no app

- Corrigido o redirecionamento do cadastro de candidato: etapa profissional agora segue para certificacoes, nao volta para dados pessoais.
- Fechado o login publico de candidato sem senha.
- Removida a exposicao de tokens de autenticacao em links gerados pela navegacao do app.
- Adicionada configuracao de URL base via `st.secrets["app"]["base_url"]`.
- Adicionado suporte a `sheet_id` e `sheet_name` configuraveis.
- Triagem assistida agora considera `experiencia_orgaos`.
- Padronizado e-mail de redefinicao com marca SeleJur.
- Senha de recrutador agora segue regra forte equivalente ao candidato.
- CPF passa a ser salvo de forma mascarada no MVP.
- Adicionados avisos de finalidade/LGPD antes da coleta de dados pessoais.
- Adicionados avisos sobre foto/documentos enquanto nao houver storage proprio.
- Adicionado aviso DISC/IA no painel de triagem do recrutador.
- Edicao de Seletivo passou a usar `batch_update`.
- Banco de candidatos passa a exibir amostra inicial em vez de tela vazia.
- Corrigida mensagem corrompida no fluxo de video.

## Ainda limitado no MVP Streamlit/Sheets

- Google Sheets continua sem escrita transacional; inscricoes simultaneas podem conflitar em alto volume.
- Fotos, documentos e videos devem migrar para storage proprio antes de uso real.
- Termos e Politica de Privacidade ainda precisam de revisao juridica final antes de uso comercial.
- A autenticacao continua sendo paliativa de MVP; a Fase 2 deve migrar para Supabase Auth.
- Perguntas customizadas por Seletivo, curriculo contextual e consentimento especifico de video ainda precisam de modelagem propria.
