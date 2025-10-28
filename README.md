# Website da ONG Transformar - Projeto de Desenvolvimento Front-End

Este repositório representa a consolidação e profissionalização do website da ONG Transformar, aplicando práticas de versionamento, acessibilidade e otimização, conforme as diretrizes da entrega final da disciplina de Desenvolvimento Front-End.

## Visão Geral do Projeto

O projeto consiste na criação do website para a ONG "Transformar", uma organização focada em impacto social. O site é composto por três seções principais: uma página inicial de apresentação, uma seção que detalha os projetos da ONG, e um formulário para cadastro de novos voluntários. O foco desta entrega final é garantir que o projeto não seja apenas funcional, mas também robusto, acessível a todos os usuários e versionado de maneira profissional.

## Deploy e Demonstração

Uma versão de produção deste projeto está disponível para avaliação no seguinte link:

- **Link da Aplicação:** [**INSIRA O LINK DO SEU DEPLOY AQUI (ex: Vercel, Netlify, GitHub Pages)**]

---

## Especificações Técnicas e Estratégias Adotadas

Esta seção detalha as estratégias implementadas para cumprir os requisitos técnicos obrigatórios.

### 1. Controle de Versão com Git/GitHub

Para garantir um ciclo de desenvolvimento organizado e rastreável, adotamos as seguintes práticas:

-   **Estratégia de Branching (GitFlow):** O desenvolvimento segue o modelo GitFlow, utilizando as seguintes branches:
    -   `main`: Contém o código de produção estável (releases).
    -   `develop`: Branch de desenvolvimento principal que integra as novas funcionalidades.
    -   `feature/*`: Branches para novas funcionalidades (ex: `feature/modo-noturno`).
    -   `release/*`: Branches para preparar uma nova versão de produção.
    -   `hotfix/*`: Branches para correções críticas em produção.

-   **Commits Semânticos:** Todos os commits seguem a convenção de [Commits Convencionais](https://www.conventionalcommits.org/en/v1.0.0/) para criar um histórico claro e legível.
    -   *Exemplo:* `feat: adiciona formulário de cadastro de voluntários`
    -   *Exemplo:* `fix: corrige problema de contraste no rodapé`

-   **Releases e Versionamento Semântico (SemVer):** As versões do projeto seguem o padrão `MAJOR.MINOR.PATCH` (ex: `v1.2.1`). As releases são criadas no GitHub a partir da branch `main`.

### 2. Acessibilidade (Conformidade WCAG 2.1 Nível AA)

O compromisso com a acessibilidade é um pilar deste projeto. As seguintes diretrizes foram estabelecidas:

-   **Navegação por Teclado:** Todos os elementos interativos são totalmente acessíveis e operáveis utilizando apenas o teclado, com indicadores de foco visíveis.
-   **Estrutura Semântica:** O HTML foi estruturado utilizando tags semânticas (`<header>`, `<main>`, `<nav>`, `<footer>`) para dar significado e contexto ao conteúdo.
-   **Contraste de Cores:** O design respeita o contraste mínimo de 4.5:1 para textos.
-   **Suporte a Leitores de Tela:** Atributos ARIA são utilizados quando necessário e todas as imagens possuem atributos `alt` descritivos.
-   **Modo Escuro e Alto Contraste:** O projeto inclui temas alternativos para melhor experiência do usuário.

### 3. Otimização para Produção

-   **Minificação:** Os arquivos CSS, JavaScript e HTML são minificados para reduzir seu tamanho.
-   **Compressão de Imagens:** As imagens (WEBP, JPG, PNG) são comprimidas e otimizadas para a web.

---
