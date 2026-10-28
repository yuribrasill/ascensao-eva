# ASCENSÃO + EVA

Aplicativo pessoal de missões e progresso, com assistente de voz local e preparação para IA conversacional.

## Publicação

O frontend é um PWA estático. Para publicar, envie `index.html`, `manifest.webmanifest`, `sw.js` e a pasta `icons/` para a raiz do repositório. Em **Settings → Pages**, selecione **Deploy from a branch**, branch `main`, pasta `/(root)`.

**Não publique o conteúdo de `server/.env` ou chaves da API OpenAI.** A pasta `server/` é apenas um exemplo de backend e não funciona no GitHub Pages.

## Instalação Android

Após publicar o GitHub Pages, abra o endereço HTTPS no Chrome e use o menu **Instalar aplicativo** ou **Adicionar à tela inicial**. O microfone requer permissão e não oferece escuta persistente em segundo plano nesta versão.

## Progresso

O progresso é salvo localmente por origem. Faça backup antes de trocar o endereço do aplicativo.
