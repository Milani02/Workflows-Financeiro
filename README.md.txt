# Workflows de Automação Financeira e de Estoque

Este repositório contém workflows (fluxos de trabalho) criados na plataforma **n8n** para automatizar tarefas financeiras e de controle de estoque. O objetivo é otimizar o envio de alertas e relatórios importantes, garantindo mais agilidade e precisão nas operações.

---

## Projetos (Workflows)

O repositório inclui três workflows principais, salvos como arquivos `.json`, cada um com uma funcionalidade específica:

### 1. Alerta de Títulos Vencidos (Individual)
- **Arquivo:** `Disparo - financeiro - 4 empresas.json`
- **Funcionalidade:** Este workflow automatiza o envio de alertas por e-mail para clientes com títulos em atraso. Ele busca no sistema os títulos que estão vencidos há **1 dia** e **18 dias** e dispara um e-mail individual para cada cliente, cobrando a regularização. O processo é configurado para quatro empresas: D.P.O, Biodinâmica, Multibrasil e Injecta.

### 2. Tabela Completa de Títulos Vencidos
- **Arquivo:** `Disparo financeiro - Tabela completa vencidos.json`
- **Funcionalidade:** Desenvolvido para uso interno, este workflow busca todos os títulos vencidos no sistema e compila uma tabela completa. Ele envia a tabela por e-mail para a equipe interna de gestão financeira, servindo como um relatório diário de acompanhamento.

### 3. Alerta de Estoque Baixo
- **Arquivo:** `Disparo de email.json`
- **Funcionalidade:** Este workflow monitora o estoque de produtos e envia um alerta quando o nível de estoque de um item atinge um ponto crítico (3 unidades ou menos). Isso garante que a equipe de gestão de estoque seja notificada a tempo para realizar a reposição necessária.

---

## Tecnologias Utilizadas

- **n8n:** Plataforma de automação de código aberto.
- **API TOTVS Rest:** Utilizada para buscar dados de títulos e produtos diretamente do sistema.
- **SMTP:** Protocolo para envio de e-mails de alerta e notificação.

## Como Usar

1.  **Importar Workflows:** Na sua instância do n8n, importe os arquivos `.json` para carregar os fluxos de trabalho.
2.  **Configurar Credenciais:** Certifique-se de que as credenciais da **API TOTVS Rest** e do **servidor SMTP** estejam configuradas corretamente no n8n.
3.  **Ativar e Agendar:** Ative os workflows e configure os gatilhos de agendamento conforme necessário para os disparos automáticos.

**Observação de Segurança:** Os arquivos `.json` não contêm credenciais sensíveis (como senhas da API ou do SMTP). Eles apenas fazem referência às credenciais armazenadas de forma segura na sua plataforma n8n.