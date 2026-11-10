# PRE681 — Separação entre Actions público e Kaggle privado

Data: 2026-11-10.

## Evidência disponível

- Repositório público criado: `Juniklx/nfsmw` (visibilidade `public` verificada via API).
- Workflow mínimo criado: `.github/workflows/nfsmw-public-runner-probe.yml`, commit `d3f06d0f020953f902bff5d7c0034d526ce11c6e`.
- O usuário informou que a execução do GitHub Actions apareceu como `Success`.
- **Limite**: ID da execução e logs não foram lidos independentemente nesta etapa; classificar como `SUCCESS_REPORTED_BY_USER`, não como log auditado.
- O repositório antigo `Juniklx/nfsmw-actions-teste` permanece privado. Os jobs privados reportaram bloqueio por pagamentos/limite de gastos; não atribuir erro ao código do jogo.

## Regra de separação

- GitHub público: verificações independentes de dados privados, documentação pública revisada, testes de runner sem segredos e sem checkout desnecessário.
- Kaggle privado: PRE681 de leitura da V51 assinada, snapshot de fonte autorizado e log PRE656 do Galaxy S24 FE obtidos pelo Google Drive com autenticação. Conservar o Drive como repositório canônico de logs/artefatos privados.
- Nunca copiar para este repositório ISO/XEX/arquivos originais do jogo, APK, saves, logs privados, chaves de assinatura, tokens, arquivos de configuração com credenciais, nem fontes cujo direito de divulgação não tenha sido confirmado.
- `.gitignore` ajuda contra acidentes mas **não é controle de segurança**: verificar conteúdos e histórico antes de publicar qualquer arquivo.

## Próxima confirmação

1. Capturar ID/URL e resultado detalhado da execução pública para validar logs e job sem depender apenas da UI relatada.
2. Executar a PRE681 no Kaggle e verificar os hashes dos arquivos originais e o retorno ao Drive.
3. Atualizar `NFSMW_Android/CONTEXTO_NFSMW.md` com evidências observadas, ressalvas e caminhos reais.

Sem nova build, patch, alteração gráfica, troca de assinatura ou alegação de ganho de FPS.
