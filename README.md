# 🚀 SmartLeads AI: Automação de Triagem e Conversão

> **Eficiência Operacional impulsionada por IA.** Transforme leads frios em agendamentos qualificados 24/7, sem intervenção humana inicial.

---

## 🎯 Visão Geral do Produto
O **SmartLeads AI** não é apenas um chatbot; é um ecossistema de triagem inteligente projetado para o mercado brasileiro (Clínicas, Escritórios Jurídicos e Consultorias). 

Focamos em **ROI (Retorno sobre Investimento)** imediato:
1.  **Redução de CAC (Custo de Aquisição de Cliente):** Elimina o tempo humano gasto em leads desqualificados.
2.  **Aumento de Conversão:** Resposta instantânea e contextualmente humana via GPT-4o.
3.  **Gestão Transparente:** O cliente final gerencia tudo via Airtable, sem precisar de painéis administrativos complexos.

---

## 🛠️ Tech Stack & Arquitetura (2026)

Esta solução utiliza uma arquitetura *Low-Code/Pro-Code Hybrid* para maximizar a velocidade de entrega sem sacrificar a flexibilidade lógica.

### 🧠 Inteligência & Orquestração
* **[n8n](https://n8n.io/)**: *O Maestro.* Atua como o backend lógico. Escolhido por permitir fluxos complexos visualmente, mas aceitar nós de *JavaScript* puro para manipulação avançada de dados, eliminando a necessidade de servidores API tradicionais.
* **[OpenAI API](https://openai.com/) (GPT-4o)**: *O Cérebro.* Utilizado não apenas para chat, mas para **Análise de Intenção** e estruturação de dados não estruturados em JSON rígido para o banco de dados.

### 🗣️ Interface & Comunicação
* **[Typebot](https://typebot.io/)**: *A Entrada.* Interface conversacional ultra-rápida. Escolhido pela UX superior aos formulários tradicionais, aumentando a taxa de preenchimento em dispositivos móveis.
* **[Evolution API](https://doc.evolution-api.com/)**: *A Conexão.* Integração nativa com WhatsApp, permitindo que a automação "viva" onde o cliente brasileiro está.

### 💾 Dados & Infraestrutura
* **[Airtable](https://airtable.com/)**: *O Banco de Dados "Cliente-Friendly".* Atua como CRM e Banco Relacional. Escolhido para eliminar a construção de dashboards customizados; o cliente visualiza, edita e aprova leads diretamente na interface do Airtable.
* **[Project IDX](https://idx.dev/) + [Firebase](https://firebase.google.com/)**: *O Ambiente.* Desenvolvimento em nuvem assistido por IA e hospedagem serverless para webhooks críticos e landing pages de alta disponibilidade.

---

## 🔄 Fluxo de Dados (Workflow)

```mermaid
graph TD
    A[Usuario Clica no Link/Ads] -->|Acesso| B(Typebot: Coleta Inicial)
    B -->|Dados Brutos| C{n8n: Orquestrador}
    C -->|Prompt Contextual| D[OpenAI GPT-4o]
    D -->|JSON Estruturado + Score| C
    C -->|Gravação| E[(Airtable: CRM)]
    C -->|Notificação| F[WhatsApp Business / Evolution API]
    E -->|Status Atualizado| G[Equipe Comercial Assume]
