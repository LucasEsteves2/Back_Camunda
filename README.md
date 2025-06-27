# CreditProcessIntegration-Camunda-Azure

Este projeto demonstra uma arquitetura de **integração entre o Camunda e aplicações em .NET** utilizando **Azure Functions** e **Azure Service Bus**, com foco em simular um fluxo automatizado de análise de crédito. A principal ênfase está na **integração técnica e orquestração de processos**, não no domínio da lógica de negócio em si.

---

## 🚀 Objetivo

O principal objetivo é demonstrar como:

- Iniciar processos BPMN no **Camunda** via REST API.
- Modelar tarefas de serviço no BPMN que são escutadas por **Azure Functions** configuradas com **Service Bus** (filas).
- Simular um fluxo assíncrono e desacoplado usando mensageria e orquestração externa.

---

## 🧩 Arquitetura

```text
[Azure Function (HTTP Trigger)] --> Inicia processo Camunda via REST API
                            ↓
[Camunda BPMN] --> envia mensagens para filas (Azure Service Bus)
                            ↓
[Azure Function (Service Bus Trigger)] --> escuta e trata as mensagens

```
## 🛠️ Tecnologias Utilizadas

### Backend & Orquestração
- **ASP.NET Core**
- **Azure Functions**
  - HTTP Trigger
  - Service Bus Trigger
- **Camunda BPM** (versão 7.x)
- **Camunda REST API**

### Mensageria
- **Azure Service Bus** (Filas)

### Linguagens & Formatos
- **C#**
- **JSON**

### Bibliotecas
- **Newtonsoft.Json**

### Infraestrutura
- **Camunda Self-hosted**
- **Azure (Functions, Service Bus)**
