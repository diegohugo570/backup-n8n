# 🤖 Portfólio de Automações com n8n + IA

Este repositório reúne **workflows avançados desenvolvidos no n8n**, com foco em **automação inteligente, agentes de IA, marketing digital e integração entre plataformas**.

Os fluxos aqui apresentados representam **casos reais de uso**, prontos para estudo, adaptação ou implementação em ambientes produtivos.

---

## 🚀 O que você vai encontrar aqui

### 🧠 Agentes de IA & Multi-Agent
- **Agentes de IA com n8n**
- **Arquiteturas Multi-Agent**
- Integração com LLMs (OpenAI / similares)
- Orquestração de decisões automáticas

---

### 📣 Marketing Digital Automatizado
- **Automação de LinkedIn com IA**
  - Criação, resposta e interação automatizada
- **Instagram com IA**
  - Responder comentários automaticamente
  - Templates inteligentes de interação
- **Geradores de conteúdo automatizados**

---

### 📲 Mensageria & Notificações
- **Registro de faturas no Telegram**
- Alertas automáticos
- Integração entre sistemas internos e canais de comunicação

---

### ⚙️ Infraestrutura & Templates
- Templates reutilizáveis de automação
- Estruturas base para novos projetos
- Backup e versionamento de workflows n8n no GitHub

---

## 🛠️ Tecnologias Utilizadas
- n8n  
- APIs REST  
- Webhooks  
- OpenAI / LLMs  
- Instagram API  
- LinkedIn Automation  
- Telegram Bot API  
- JSON / HTTP / OAuth  

---

## 🎯 Objetivo do Repositório
Este repositório tem como finalidade:
- Servir como **portfólio técnico**
- Demonstrar **capacidade de automação real**
- Acelerar novos projetos com **templates prontos**
- Compartilhar boas práticas em automações com IA

---

## 📂 Projetos em Destaque

### 🤖 Potto Flow – Agente com Follow Up Inteligente (WhatsApp)

![Potto Flow - Agente com Follow Up](./Agente%20com%20follow%20up.png)

**Descrição:**  
Workflow avançado de **Agente de IA com Follow Up automático**, desenvolvido no **n8n**, focado em **atendimento, qualificação e reengajamento de leads via WhatsApp**.

Este projeto simula um **assistente humano**, com **memória de conversa, entendimento de intenção do usuário e automações de acompanhamento temporal**, sendo ideal para clínicas, vendas, suporte ou pré-atendimento.

**O que esse agente faz na prática:**
- Recebe mensagens via **Webhook (WhatsApp API)**
- Filtra mensagens válidas (ignora grupos, edições, newsletters e mensagens próprias)
- Cria ou recupera usuários automaticamente no **Supabase**
- Interpreta mensagens em **texto, áudio ou imagem**
  - Áudio → transcrição automática com IA
- Utiliza **Agente de IA (LLM)** com:
  - Prompt estruturado
  - Memória de conversa por usuário
  - Ferramenta de escrita no banco (Tool Calling)
- Identifica o **desejo/intenção do usuário** (ex: agendamento)
- Responde de forma natural e contextual via **WhatsApp**
- Atualiza histórico, última interação e estágio do lead no banco
- Executa **Follow Ups automáticos**:
  - ⏱️ Após 10 minutos
  - ⏱️ Após 24 horas
  - ⏱️ Após 3 dias
- Evita mensagens repetidas usando controle de **etapas**
- Totalmente orientado a **experiência do usuário e conversão**

**Stack utilizada:**
- n8n  
- Webhooks  
- OpenAI (LLM + Transcrição de Áudio)  
- Supabase (Database + Tool Calling)  
- WhatsApp API (Z-API)  
- Memory Buffer (contexto por usuário)  
- Automação baseada em tempo (Schedule Trigger)

**Casos de uso reais:**
- Clínicas e consultórios  
- SDR e pré-vendas automatizado  
- Atendimento inteligente no WhatsApp  
- Follow up de leads sem intervenção humana  
- Redução de abandono de conversas  

📁 **Arquivo do workflow incluso no repositório:**  
`Potto_Flow___Agente_com_Follow_Up.json`

---

## 👤 Autor
**Diego Hugo**  
Especialista em Inteligência Artificial com foco em **Automações Inteligentes, Agentes Autônomos e Python**

📌 Áreas de atuação:
- IA Generativa  
- Agentes Autônomos (LangGraph)  
- RAG  
- Automação Inteligente (Python / n8n)  
- Aplicações reais de IA para empresas

🔹 Especialidades:
- Automação Inteligente
- Agentes Autônomos
- n8n avançado
- IA aplicada a marketing e operações

---

## ⚠️ Observações Importantes
- Os arquivos representam **exports de workflows do n8n**
- Alguns fluxos podem exigir:
  - Credenciais (APIs)
  - Ajustes de variáveis de ambiente
- Recomenda-se importar os workflows em ambiente de teste antes de produção

---

🚀 Sinta-se à vontade para explorar, adaptar e evoluir essas automações.
