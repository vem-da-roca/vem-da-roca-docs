# 🌱 Vem da Roça — Documentos legais

O **Vem da Roça** é um marketplace que aproxima consumidores de produtores rurais. Este diretório reúne a Política de Privacidade e os Termos e Condições do aplicativo, publicados como páginas web para consulta dos usuários e para informar as lojas de aplicativos.

## 🗂️ Estrutura do projeto

O diretório de trabalho agrupa os projetos de front-end, back-end e documentação legal. É uma **pasta unificada de projetos independentes**, não um único repositório Git monolítico:

```text
Flutter e Backend/
├── vem-da-roca-flutter/       # Aplicativo móvel e Web em Flutter
├── vem-da-roca-api/           # API REST do marketplace
└── vem-da-roca-docs/          # Documentos legais publicados na Web
    ├── README.md
    ├── privacidade.html
    └── termos.html
```

O aplicativo Flutter consome a API REST para autenticação, catálogo e demais recursos do marketplace. Os documentos HTML desta pasta são destinados à publicação no GitHub Pages; suas URLs públicas podem ser usadas como links web no aplicativo para que os usuários consultem os textos.

## ⚖️ Documentação legal e compliance

- [`privacidade.html`](./privacidade.html) — descreve o tratamento de dados pessoais, localização, direitos dos titulares, retenção e exclusão de dados.
- [`termos.html`](./termos.html) — apresenta as condições de uso do aplicativo, incluindo licença, responsabilidades e regras de utilização.

As páginas públicas também podem ser informadas à Google Play e à Apple App Store nos campos de política de privacidade e termos aplicáveis. Após publicar este diretório no GitHub Pages, substitua os marcadores pelas URLs definitivas:

- **Política de Privacidade:** [INSERIR LINK]
- **Termos e Condições:** [INSERIR LINK]

> Confirme que o GitHub Pages está habilitado para o repositório e teste as URLs em uma janela anônima antes de cadastrá-las nas lojas.

## 🧰 Tecnologias utilizadas

- **Front-end:** Flutter e Dart.
- **Back-end:** [INSERIR TECNOLOGIAS DO BACK-END].
- **Documentação legal:** HTML e CSS.
- **Hospedagem pública dos documentos:** GitHub Pages.

## 🚀 Como executar

### Aplicativo Flutter

Consulte o [README do front-end](../vem-da-roca-flutter/README.md) para requisitos, instalação e demais opções de execução. No Linux, para iniciar a versão Web usando a API local:

```bash
cd vem-da-roca-flutter
flutter pub get
flutter run -d web-server --web-hostname=127.0.0.1 --web-port=5000 \
  --dart-define=API_URL=http://localhost:3330
```

Abra `http://127.0.0.1:5000` no navegador. Para iniciar a API local ou consultar a opção de API fictícia, siga as instruções dos READMEs do [back-end](../vem-da-roca-api/README.md) e do [front-end](../vem-da-roca-flutter/README.md).

### Documentos legais

Os arquivos HTML são páginas estáticas: podem ser abertos diretamente no navegador ou servidos pelo GitHub Pages. Não precisam de instalação de dependências para visualização.
