# Página de Vendas — Palavras Hebraicas + Mini App

Página estática em um único arquivo HTML. Sem build, sem frameworks e sem dependências externas.

## Links importantes

- **Site publicado (Vercel):** https://palavras-hebraicas-vendas.vercel.app
- **Repositório GitHub:** https://github.com/crieia2024-bot/palavras-hebraicas-vendas
- **Mini App Interativo de Demonstração:** https://ebook-palavras-hebraicas.vercel.app/
- **Checkout:** Configure o link do checkout nos botões de compra (`href` em `index.html`).

---

## Como trocar o preço

O preço aparece no cabeçalho Hero, no fechamento e na barra fixa do celular:

```bash
grep -Fn 'R$ 19,90' index.html
```

---

## Visualização local

```bash
cd /Users/juananjos/Documents/pagina-vendas-hebraico && python3 -m http.server 4400
```
Abra `http://localhost:4400` no navegador e ative o modo celular (DevTools).

---

## Publicar / Atualizar na Vercel

```bash
cd /Users/juananjos/Documents/pagina-vendas-hebraico
git init
git add .
git commit -m "Página de vendas Palavras Hebraicas"
gh repo create palavras-hebraicas-vendas --public --source=. --push
vercel --prod --yes
```

---

## Imagens e recursos

Todos os recursos estão em `img/`:
- `logo.png` / `favicon.png` / `apple-touch-icon.png` — Logo e ícones oficiais.
- `capa.jpg` — Capa oficial do livro Palavras Hebraicas.
- `app_*.jpg` — Screenshots do Mini App leitor interativo no celular e desktop.
- `p_*.jpg` — 6 páginas de demonstração interna extraídas de `PALAVRAS_HEBRAICAS.pdf` (Chesed, Shalom, Shema, Elohim, Alefbet e Letra Álef).
