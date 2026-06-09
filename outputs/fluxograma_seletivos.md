# Fluxograma Proposto - Seletivos JurisBank

```mermaid
flowchart TD
    A["Recrutador cria Seletivo"] --> B["Define dados da vaga: orgao, area, regime, remuneracao, prazo"]
    B --> C["Define criterios objetivos: requisitos, experiencia, sistemas, OAB, instituicoes de interesse"]
    C --> D["Define etapas: curriculo, entrevista, teste de escrita, prova pratica, referencias, periodo de experiencia"]
    D --> E["Define matriz de pontuacao e mensagem aos candidatos"]
    E --> F["Publica Seletivo"]

    F --> G["Sistema cruza preferencias dos interessados e candidatos ativos"]
    G --> H["Aviso basico para interessados ainda sem cadastro completo"]
    G --> I["Aviso direto para candidatos ativos compativeis"]

    H --> J["Interessado faz cadastro completo"]
    J --> K["Pagamento/inscricao no Seletivo"]
    I --> K

    K --> L["Recrutador visualiza inscritos em painel"]
    L --> M["Triagem por filtros e matriz"]
    M --> N["Lista curta de candidatos"]
    N --> O{"Etapas adicionais?"}
    O -- "Entrevista" --> P["Registrar notas de entrevista"]
    O -- "Teste/prova" --> Q["Registrar resultado do teste"]
    O -- "Referencias" --> R["Registrar checagem de referencias"]
    O -- "Periodo de experiencia" --> S["Registrar avaliacao do periodo"]
    O -- "Nao" --> T["Decisao final"]
    P --> T
    Q --> T
    R --> T
    S --> T
    T --> U["Encerrar Seletivo com historico interno"]
```

## Pontos Para Validar

- O pagamento acontece no momento da inscricao no Seletivo, nao no cadastro basico de avisos.
- O cadastro basico apenas captura interesse e permite aviso de compatibilidade.
- O cadastro completo e necessario para participar e compartilhar perfil com recrutador.
- O recrutador precisa de poucos campos obrigatorios, mas suficientes para dar confianca: criterios, etapas e matriz.
- A decisao final continua humana; o JurisBank organiza informacoes, filtros e historico.
