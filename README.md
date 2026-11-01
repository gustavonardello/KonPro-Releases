# KonPro — instaladores

**KonPro** (Konvos e Projetos) é um aplicativo desktop para Windows que organiza atendimentos diários,
DAGs, projetos, pendências e acessos de clientes. Os dados ficam só no seu computador, num banco
criptografado com a sua senha mestra.

Este repositório público contém **apenas os instaladores e pacotes de atualização**. O código-fonte é
mantido em um repositório privado.

## Instalar

1. Abra a página de [Releases](https://github.com/gustavonardello/KonPro-Releases/releases/latest).
2. Baixe **`KonProApp-win-Setup.exe`** e execute.
3. O Windows SmartScreen pode avisar "O Windows protegeu o computador", porque o instalador não tem
   assinatura digital. Clique em **Mais informações → Executar assim mesmo**.
4. No primeiro uso, crie a **senha mestra**. Ela é a chave do banco: **sem ela não há como recuperar os
   dados**. Guarde-a num gerenciador de senhas (ex.: Bitwarden).

**Requisitos:** Windows 10 ou 11 (64 bits) com o Microsoft Edge WebView2 Runtime (já presente nas versões
atualizadas do Windows). Não é preciso instalar o .NET: ele vem junto com o aplicativo.

## Atualizar

O KonPro verifica novas versões ao abrir e mostra o aviso **"Versão X disponível — Atualizar e
reiniciar"**. Antes de atualizar, ele faz um backup do banco e fecha o cofre. Também é possível verificar
em **Configurações → Sobre → Verificar atualização agora**.

## Onde ficam os arquivos

| O quê | Pasta |
|---|---|
| Aplicativo | `%LOCALAPPDATA%\KonProApp` |
| Banco criptografado e backups automáticos | `%LOCALAPPDATA%\KonPro` |
| Backups manuais | a pasta escolhida em **Configurações** (ex.: OneDrive) |

Atualizar ou desinstalar o aplicativo **não apaga** o banco nem os backups.

## Integração com Claude e Codex (MCP)

O instalador inclui `KonPro.Mcp.exe`, que permite consultar e registrar informações pelo Claude Desktop,
Claude Code ou Codex enquanto o KonPro estiver aberto e desbloqueado. O caminho exato aparece em
**Configurações → Sobre**, com botão para copiar. A gravação de dados pelo chat vem desligada e pode ser
ativada em **Configurações**.

## Novidades

As mudanças de cada versão estão nas notas de cada [release](https://github.com/gustavonardello/KonPro-Releases/releases).
