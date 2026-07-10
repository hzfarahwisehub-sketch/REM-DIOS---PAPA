# Remédios do Pai — PWA (Família Farah)

App de acompanhamento dos medicamentos, instalável no iPhone e Android, funciona offline, grátis.

## O que tem
- Cronograma por horário, com marcação de "dado hoje".
- **Editar / adicionar / apagar** horários e medicamentos (botão *Editar*).
- **3 temas**: Claro, Meio a meio, Escuro.
- **Alarme dentro do app** (som gerado + vibração + notificação) enquanto aberto.
- **Calendário .ics** e **guia do app Relógio** para o alarme nativo do celular (botão *Mais*).
- **Backup**: exportar/importar a lista em JSON.

## Publicar no GitHub Pages (grátis)
1. Criar um repositório (pode ser público; **não há segredo nenhum** aqui — os dados de cada
   pessoa ficam só no navegador dela).
2. Subir todo o conteúdo desta pasta na raiz do repositório.
3. Settings → Pages → Source: `main` / root → Save.
4. Abrir a URL `https://SEU-USUARIO.github.io/NOME-DO-REPO/` no **Chrome (Android)** ou **Safari (iPhone)**.
5. Instalar: Android → menu ⋮ → "Adicionar à tela de início"; iPhone → Compartilhar → "Adicionar à Tela de Início".

## Arquivos
- `index.html` — o app (HTML+CSS+JS, sem dependências externas).
- `manifest.json` — metadados do PWA.
- `sw.js` — service worker (cache offline + suporte a push na fase 2).
- `icons/` — ícones do app.

## Fase 2 (push no Android, opcional)
`sw.js` já trata `push` e `notificationclick`. Falta: gerar chaves VAPID, um botão de
inscrição no app, e um agendador grátis (GitHub Actions cron) que envie o push nos horários.

_Feito por Friday para Hammis Farah. Ferramenta de apoio; a prescrição é sempre do médico._
