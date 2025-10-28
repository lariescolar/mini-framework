# 💻 Aula 9 — Mini-Framework Responsivo Final

Nesta atividade você vai **pegar um código inicial (HTML + CSS)**, fazer uma **cópia** e **evoluir** esse código para montar uma **interface simples de blog/artigo**, igual a imagem de referência.

## 🎯 Objetivo
Finalizar e aplicar um **mini-framework CSS** (classes utilitárias) para construir uma página **responsiva**, clara e organizada.

## 🧠 O que você vai treinar
1. **Consolidar** classes utilitárias (tipografia, cores, espaçamentos, containers flex).  
2. **Criar/usar** classes de responsividade (ex.: `.col-6`, `.col-12`, `.hide-mobile`).  
3. **Documentar** o framework (comentários no CSS e um README curto).

---

## 🖼️ O layout (o que a página deve ter)
- **Header** com título do site, busca/links.  
- **Título do artigo** bem destacado, com info do autor/data.  
- **Trecho de texto** com link “Continuar lendo”.  
- **Lista de categorias/tags** em chips (etiquetas).  
- **Espaçamentos coerentes**, cores básicas (tons de **vermelho** e **cinza**) e **responsividade**.

---

## 🗂️ Organização dos arquivos
Crie/garanta esta estrutura no seu repositório (branch `bimestre-3`):

bimestre-3/
|__Atividade 9 - Mini Framework
   |__ index.html
   |__ framework.css
   |__ README.md


---

## 🛠️ Passo a passo (em sala)

1) **Copiar o código base**  
   - Baixe ou clone o projeto inicial disponibilizado.  
   - Crie a pasta **Atividade 9 - Mini Framework** e coloque os arquivos lá.

2) **Abrir no VS Code**  
   - Abra a pasta da atividade no VS Code.  
   - Se puder, use o **Live Server** (plugin) para visualizar em tempo real.

3) **Conectar o CSS**  
   - Garanta que o `index.html` tenha:  
     ```html
     <!-- o framework é seu, deu um nome melhor que framework -->
     <link rel="stylesheet" href="framework.css">
     <meta name="viewport" content="width=device-width, initial-scale=1">
     ```

4) **Completar o HTML**  
   Monte as seções principais (pode usar as classes utilitárias já criadas por você):  
   - `<header>` com título + navegação.  
   - `<main>` com `<article>`, título `<h1>`, subtítulo/autor, parágrafos e link “continuar lendo”.  
   - Lista de **categorias** (chips) — pode ser `<ul>` com `<li>`.

5) **Evoluir o mini-framework** (`framework.css`)  
   - **Reset** (se necessário):  
     ```css
     *{box-sizing:border-box;margin:0;padding:0}
     img{max-width:100%;display:block}
     body{font:16px/1.6 system-ui, sans-serif; color:#374151; background:#f6f7f8;}
     ```


   - **Utilitários de tipografia e espaçamento**:  
     ```css
     .h1{font-size:2rem;font-weight:800}
     .muted{color:#6b7280}
     .mt-2{margin-top:.5rem}.mt-4{margin-top:1rem}
     .mb-2{margin-bottom:.5rem}.mb-4{margin-bottom:1rem}
     .p-2{padding:.5rem}.p-3{padding:1rem}
     .text-center{text-align:center}
     ```


   - **Cores/realces**:  
     ```css
     .primary{color:#c62828}
     .chip{border:1px solid #e57373;border-radius:999px;padding:.25rem .5rem;color:#c62828;background:#fff}
     ```

   - **Layout (flex + container)**:  
     ```css
     .container{max-width:1100px;margin-inline:auto;padding-inline:1rem}
     .flex{display:flex}
     .items-center{align-items:center}
     .between{justify-content:space-between}
     .gap-2{gap:.5rem}
     ```

   - **Responsividade (mobile-first)**:  
     ```css
     .row{
         display:flex;
         flex-wrap:wrap;
         gap:1rem
      }
     .col-12{flex:1 1 100%}
     .col-6{flex:1 1 100%} /* mobile */

     @media (min-width:768px){
       .col-6{flex:1 1 calc(50% - 1rem)}
       .hide-mobile{display:none}
     }
     @media (min-width:1024px){
       .h1{font-size:2.5rem}
     }
     ```
   - **Chips/tags** (lista horizontal):  
     ```css
     .chips{display:flex;flex-wrap:wrap;gap:.5rem}
     ```

6) **Aplicar as classes no HTML**  
   - Use `.container`, `.h1`, `.muted`, `.chips`, `.chip`, `.mt-*`, `.mb-*`, etc.  
   - Ajuste margens e tamanhos até ficar parecido com a referência.
  

7) **Testar responsividade**  
   - Abra o **DevTools** (F12) → modo mobile.  
   - Verifique 375px (celular), 768px (tablet) e 1366px (desktop).  
   - Ajuste o que “quebrar”.

8) **Documentar**  
   - No `README.md`, liste as classes criadas/alteradas e **como usar** (ex.: `.chip`, `.chips`, `.between`, `.col-6`, etc).

9) **Commit e Push**  
   - Faça commits curtos e claros (ex.: `feat(css): adiciona utilitários de chip e grid`).
   - **Push** para a branch `bimestre-3`.

10) **Entregar no Classroom**  
   - Envie o **link da pasta** `Atividade 9 - Mini Framework`.

---

## Checklist de conclusão (em sala)
- [ ] HTML com **header, article** e **categorias**  
- [ ] `framework.css` com **utilitários** (tipografia, espaçamento, cores, flex)  
- [ ] **Responsividade** funcionando (mobile → desktop)  
- [ ] **README** explicando as classes

---

> **Meta do bimestre:** seu mini-framework será a base do **projeto final**. Quanto mais bem feito hoje, mais rápido será montar e publicar seu site responsivo.
