# Núcleo E.V.A. — especificação v0.3

**E.V.A.** = Entidade Virtual de Assistência. Copiloto pessoal com estratégia, proximidade, humor inteligente e respeito à autonomia.

## Arquitetura atual
- Aplicativo HTML local: missões, XP, boss, perfil, exportação/importação e síntese de voz; persistência em `localStorage` (`ascensao-v1`).
- Modo local: reconhecimento de voz quando suportado pelo navegador, comandos limitados, sem IA generativa. O reconhecimento pode depender de serviço externo do navegador.
- Modo IA: `POST /api/eva` para backend Node com chave `OPENAI_API_KEY` exclusiva do servidor; resposta textual falada pela síntese do dispositivo.
- A IA **não** pode editar dados do jogador nesta versão.

## Personalidade
Elegante e estratégica, natural e bem-humorada, empática sem bajulação. Prioriza resultados e bem-estar, evita pressão e excesso de notificações. Não finge consciência ou acesso a outros aplicativos.

## Próxima evolução recomendada no Codex
1. Separar `index.html` em módulos e adicionar testes automatizados para XP, datas, modo leve, backups e boss.
2. Criar PWA HTTPS com manifest, ícones próprios e service worker; testar Chrome Android.
3. Criar autenticação e sincronização opcional, com controles de privacidade e exclusão de dados.
4. Adicionar ferramentas de IA de leitura e propostas de ações; execução só após confirmação explícita e validação no backend.
5. Adicionar conversação em tempo real via WebRTC com credenciais efêmeras emitidas pelo servidor, autenticação, limites e custos monitorados.
6. Integrações externas somente por permissões específicas; nenhuma chave de API no navegador.

## Limites atuais
Não há ativação contínua por palavra-chave, escuta em segundo plano, conexão automática à memória do ChatGPT, nem chamadas externas executadas pela IA. Teste em dispositivo físico ainda pendente.
