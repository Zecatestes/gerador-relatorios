# Gerador de Relatórios Odeen

Aplicação web da Odeen & Co. para geração de relatórios de recuperação de veículos e formalizações operacionais.

## O que foi preparado

Este repositório foi separado do projeto original do Replit para ficar independente e pronto para GitHub:

- aplicação React + TypeScript + Vite na raiz;
- Formalizador Faster integrado;
- imagens e arquivos públicos preservados;
- sem `api-server`, banco de dados ou serviços do Replit;
- sem cópias duplicadas dentro de `downloads/`;
- sem arquivos `.replit`;
- `.gitignore` configurado;
- workflow de GitHub Pages incluído;
- tema escuro e preferências locais preservados.

## Rodar no computador

Requer Node.js 20.19+ ou 22.12+.

```bash
npm install
npm run dev
```

Depois abra o endereço informado pelo Vite, normalmente:

`http://localhost:5173`

## Gerar versão de produção

```bash
npm run build
npm run preview
```

A versão pronta fica em:

```text
dist/
```

## Publicar no GitHub

1. Crie um repositório vazio no GitHub.
2. Envie **todo o conteúdo desta pasta**, e não a pasta ZIP.
3. Faça o primeiro commit na branch `main`.
4. O workflow `.github/workflows/deploy-pages.yml` fará o build automaticamente.
5. No GitHub, abra **Settings → Pages** e selecione **GitHub Actions** como fonte, se ainda não estiver selecionado.

Depois do primeiro deploy, o site ficará disponível na URL do GitHub Pages do repositório.

## Estrutura

```text
.
├── .github/
│   └── workflows/
│       └── deploy-pages.yml
├── public/
│   ├── formalizador-faster.html
│   ├── logo-odeen.png
│   ├── logo-odeen-capa.jpeg
│   ├── marca-dagua-odeen.jpeg
│   └── ...
├── src/
├── .env.example
├── .gitignore
├── index.html
├── package.json
├── tsconfig.json
└── vite.config.ts
```

Os dados dos relatórios são processados localmente no navegador. O projeto não depende de banco de dados ou API para gerar o PDF.
