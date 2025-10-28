## Descrição

Este Pull Request adiciona melhorias de acessibilidade (WCAG 2.1 AA), scripts de build para produção, testes automatizados de acessibilidade (pa11y e axe), workflow de CI e deploy para GitHub Pages.

## Principais mudanças

- Skip-link e landmarks semânticos nas páginas HTML.
- Atributos ARIA e suporte a navegação por teclado para menus.
- Estilos de foco visíveis e utilities de acessibilidade.
- `package.json` com scripts de build, pa11y e axe.
- Workflow GitHub Actions que executa build, pa11y/axe e publica `dist/` no GitHub Pages quando em `main`.
- Relatórios de acessibilidade gerados como artefatos no CI.

## Checklist de revisão

- [ ] Rodar `npm install` e `npm run build` localmente e verificar `dist/`.
- [ ] Executar `npm run test:a11y` e `npm run test:axe` localmente (com servidor `npm run serve:dist` em execução).
- [ ] Revisar relatórios `pa11y-report-*.html` e `axe-report-*.html` (no CI estarão em Artifacts).
- [ ] Revisar código e testá-lo com teclado e leitor de tela.

## Como testar (resumo rápido)

1. `npm install`
2. `npm run build`
3. `npm run serve:dist`
4. Em outro terminal: `npm run test:a11y:report` e `npm run test:axe:report`

## Observações

O workflow do GitHub executará as validações automaticamente em push/PR para `develop` e `main`. Se for fazer merge para `main`, o job de deploy publicará o site em GitHub Pages.
