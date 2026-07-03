# Portfólio — Marcelo Pereira

Site estático (`index.html` + `style.css`), pronto para publicar em **GitHub Pages**
no domínio `mgspereira.github.io`.

## Deploy no GitHub Pages

1. **Criar o repositório** no GitHub com o nome exato `mgspereira.github.io`
   (público — esse nome específico é obrigatório para o Pages publicar
   automaticamente na raiz do domínio).

2. **Subir os arquivos** (`index.html`, `style.css`, este `README.md`):
 
   ```bash
   cd caminho/para/portfolio
   git init
   git add .
   git commit -m "Primeira versão do portfólio"
   git branch -M main
   git remote add origin https://github.com/mgspereira/mgspereira.github.io.git
   git push -u origin main
   ```

3. **Ativar o GitHub Pages**: Settings → Pages → Branch: `main` / `root` → Save.
   Repositórios `usuario.github.io` costumam publicar automaticamente sem esse
   passo, mas confirme em Settings → Pages se o status está "Your site is live".

4. Acesse em `https://mgspereira.github.io` (pode levar 1–2 minutos após o push).

## Checklist de pendências

- [ ] Gerar o link **Publish to Web** do dashboard NBA no Power BI Service e
      substituir `COLE_AQUI_O_LINK_PUBLISH_TO_WEB` no `src` do `<iframe>`
      dentro do card do projeto NBA (`index.html`).
- [ ] Conferir/trocar os links de repositório de cada projeto — usei nomes
      prováveis (`nba-dashboard-2025-26`, `automacao-vagas-for-business`,
      `pipeline-recrutamento-dashboard`, `extracao-reservas-airbnb`); ajuste
      para o nome real de cada repo em `github.com/mgspereira/...`.
- [ ] Adicionar screenshots/GIFs dos dashboards nos cards de projeto
      (`.project-card`) — hoje eles têm só texto.
- [ ] Revisar a copy final (textos de "Sobre", descrições de projeto) antes
      de publicar.
- [ ] Depois de publicar, redirecionar/aposentar os portfólios antigos:
      `mgspereira.myportfolio.com` e `sites.google.com/view/mgspereira`
      (ex.: trocar bio do LinkedIn/GitHub para apontar só para o novo link).

## ⚠️ Nota de segurança — embed Power BI

O card do projeto **NBA** usa **Publish to Web**, que torna o relatório público,
sem autenticação/RLS e indexável por buscadores. Isso é aceitável **apenas**
porque os dados da NBA são públicos. **Não reutilize essa técnica** em nenhum
dashboard de Recrutamento, People Analytics ou qualquer dado corporativo
Universia/Santander — para esses casos, use apenas prints/GIFs estáticos no
card, sem embed ao vivo.

## Estrutura de arquivos

```
portfolio/
├── index.html   → página única (hero, sobre, projetos, skills, certificações, contato)
├── style.css    → design tokens, cores (#E8A33D gold / #2E7D6B teal), tipografia IBM Plex
└── README.md    → este arquivo
```
