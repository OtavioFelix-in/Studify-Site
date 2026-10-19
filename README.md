<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/logo-escuro.png" />
  <img src="assets/logo-claro.png" width="360" alt="Studify" />
</picture>

**Site de apresentação do Studify: provas, trabalhos e prazos num lugar só.**

</div>

---

## O que é

Página única que apresenta o Studify e leva para o download do APK. É o material promocional do app: mostra as telas, os GIFs do app em uso e os recursos principais, no mesmo visual do aplicativo.

## Como funciona

Site estático, sem build: só `index.html`, `style.css` e a pasta `assets/`.

- **Publicação:** GitHub Pages, a partir da branch `main` (pasta raiz). Todo push na `main` atualiza o site em cerca de 1 minuto.
- **Testar localmente:** abrir o `index.html` no navegador.
- **Tema claro e escuro:** segue o sistema, e o botão no topo alterna (a escolha fica salva no navegador). Os prints trocam junto com o tema.
- **Cores e fonte:** as mesmas do app (`src/theme.js`), definidas no topo do `style.css`. Fonte Bricolage Grotesque e ícones Lucide.

## Download do APK

Os botões de download apontam para os releases do GitHub. O repositório e o nome do arquivo ficam no topo do `<script>` do `index.html`:

```js
var RELEASES_REPO = 'OtavioFelix-in/Studify-Site'; // dono/nome do repositório com os releases
var APK_FILE = 'Studify.apk';                     // nome do arquivo anexado em cada release
```

Para lançar uma versão: crie um release no repositório e anexe o APK com esse nome. O botão "Baixar o APK" sempre pega o mais recente.

## Estrutura

```
├── index.html               # página única
├── style.css                # cores, layout e animações
└── assets/
    ├── logo-claro.png       # logo horizontal, tema claro
    ├── logo-escuro.png      # logo horizontal, tema escuro
    ├── icon.png, favicon.png
    ├── telas/               # prints do app, claro e escuro
    ├── gifs/                # o app em uso (nova tarefa, concluir, abas, tema)
    └── fontes/              # Bricolage Grotesque e ícones Lucide
```

O arquivo de ícones (`Lucide-site.ttf`) tem só os ícones usados na página, para carregar rápido. Para usar um ícone novo, gere o arquivo de novo a partir do `Lucide.ttf` completo incluindo o código dele.

---

<div align="center">Studify · feito por Otávio Felix</div>
