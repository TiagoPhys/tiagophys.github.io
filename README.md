# Site pessoal (template iPortfolio)

Site estático em HTML puro. Não precisa de Quarto nem de nenhum comando para gerar: o GitHub Pages publica os arquivos como estão.

## Estrutura

```
index.html                 página principal: capa, About, Skills, Resume, Portfolio, Research, Contact
experience.html            página detalhada da experiência na Softex
projects/*.html            uma página por projeto
assets/css/main.css        CSS original do template (não mexa)
assets/css/custom.css      minhas alterações; a cor de destaque é --accent-color
assets/img/profile.jpg     sua foto (troque pela sua, de preferência quadrada)
assets/img/hero-bg.jpg     fundo da capa (trajetórias de movimento browniano)
assets/img/projects/       miniaturas dos cards e gráficos dos projetos
files/cv.pdf               coloque seu CV aqui
```

## Ver localmente

Abra um terminal dentro desta pasta e rode:

```bash
python -m http.server 8000
```

Depois abra http://localhost:8000 no navegador. Depois de editar um arquivo, aperte F5.

## O que preencher

Procure por `[` nos arquivos `.html` (Ctrl+Shift+F no VS Code): sobrenome, link do LinkedIn, universidade e anos do doutorado, data de início na Softex e os 4 artigos.

## Publicar no GitHub Pages

1. Suba o conteúdo desta pasta para o repositório `<seu-usuario>.github.io`, na branch `main`.
2. No GitHub, vá em Settings → Pages → Source: "Deploy from a branch", branch `main`, pasta `/ (root)`.
3. Para atualizar: `git add .`, `git commit -m "..."`, `git push`. O site muda em um ou dois minutos.

Se você já publicou a versão em Quarto: apague a pasta `.github/workflows` e a branch `gh-pages`, e mude a Source do Pages para a `main`, como no passo 2.

## Adicionar um projeto

1. Copie uma página de `projects/` (por exemplo `fraud-detection.html`) com um nome novo e troque o texto.
2. Coloque os gráficos em `assets/img/projects/<nome-do-projeto>/` e a miniatura em `assets/img/projects/<nome-do-projeto>.png`. Use uma miniatura de proporção 16:10, por exemplo 1200×750.
3. Em `index.html`, copie um bloco `portfolio-item` da seção Portfolio e ajuste o título, o texto, a imagem e o link. A classe `filter-ml`, `filter-analytics` ou `filter-quant` define em qual filtro o projeto aparece.

## Licença do template

iPortfolio é um template gratuito da BootstrapMade. A licença gratuita exige manter o crédito "Designed by BootstrapMade" no rodapé. Detalhes em `assets/TEMPLATE-LICENSE.txt`.
