Descrição
Este Pull Request adiciona melhorias de acessibilidade (WCAG 2.1 AA), integração de build para produção, testes automatizados de acessibilidade (pa11y e axe), workflow de CI e deploy automático para GitHub Pages.

Principais mudanças
- Skip-link e landmarks semânticos nas páginas HTML.
- Atributos ARIA e suporte a navegação por teclado para menus.
- Estilos de foco visíveis e utilities de acessibilidade.
- Ajustes nas variáveis de cor para melhorar contraste (>=4.5:1 quando aplicável).
- `package.json` com scripts de build, pa11y e axe.
- Workflow GitHub Actions que executa build, pa11y/axe, gera relatórios e publica `dist/` no GitHub Pages quando em `main`.
- Relatórios de acessibilidade (pa11y e axe) gerados como artefatos no CI.

Checklist de revisão
- [ ] Rodar `npm install` e `npm run build` localmente e verificar `dist/`.
- [ ] Executar `npm run test:a11y` e `npm run test:axe` localmente (com servidor `npm run serve:dist` em execução).
- [ ] Revisar relatórios `pa11y-report-*.html` e `axe-report-*.html` (no CI estarão em Artifacts).
- [ ] Testar navegação por teclado e com leitor de tela (ex.: NVDA/VoiceOver).
- [ ] Validar deploy (após merge em `main`, verificar GitHub Pages).

Como testar (resumo rápido)
1. `npm install`
2. `npm run build`
3. `npm run serve:dist`
4. Em outro terminal: `npm run test:a11y:report` e `npm run test:axe:report`

Observações
- O workflow do GitHub executará as validações automaticamente em push/PR para `develop` e `main`.
- Se preferir, este PR pode ser mesclado para `develop` para integração, e depois criar uma release para `main` (seguindo GitFlow).
