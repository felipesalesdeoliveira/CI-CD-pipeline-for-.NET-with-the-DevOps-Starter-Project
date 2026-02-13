# 🚀 CI/CD para Aplicação .NET com Azure DevOps Starter

![devops](https://imgur.com/gBofYCl.png)

## 📌 Sobre o Projeto

Este projeto demonstra a criação automatizada de uma pipeline completa de CI/CD para uma aplicação ASP.NET Core utilizando o Azure DevOps Starter.

A solução provisiona automaticamente:

- Repositório Git
- Pipeline de Build (CI)
- Pipeline de Release (CD)
- Azure Web App
- Azure SQL Database
- Application Insights
- Dashboard centralizado no Azure Portal

O objetivo é simular um cenário real de entrega contínua em ambiente cloud, com deploy automatizado e monitoramento integrado.

---

# 🏗️ Arquitetura da Solução

A arquitetura contempla:

## 1️⃣ Camada de Aplicação
- ASP.NET Core MVC
- Deploy em Azure App Service (Windows)
- Integração com Azure SQL Database

## 2️⃣ Pipeline de Integração Contínua (CI)
- Restore de dependências
- Build da aplicação
- Execução de testes automatizados
- Publicação de artefatos

## 3️⃣ Pipeline de Entrega Contínua (CD)
- Provisionamento de recursos Azure
- Deploy da aplicação
- Deploy de scripts SQL
- Execução de testes pós-deploy

## 4️⃣ Observabilidade
- Azure Application Insights
- Logs de pipeline
- Histórico de releases

---

# 🧠 Decisões Técnicas

- Uso do Azure DevOps Starter para bootstrap automatizado do projeto
- Pipeline com gatilho automático (CI Trigger por commit)
- Deploy contínuo ativado via CD Trigger
- Infraestrutura provisionada automaticamente via pipeline
- Separação entre build e release para controle e rastreabilidade
- Monitoramento integrado desde o primeiro deploy

---

# ⚙️ Stack Tecnológica

- **Microsoft Azure**
  - Azure App Service
  - Azure SQL Database
  - Application Insights
- **Azure DevOps**
  - Repos
  - Pipelines (Build & Release)
- **.NET Core (ASP.NET Core MVC)**
- **Git**

---

# 🚀 Provisionamento com Azure DevOps Starter

A criação do projeto é realizada diretamente pelo Azure Portal:

1. Criar recurso **DevOps Starter**
2. Selecionar aplicação **.NET Core**
3. Escolher destino Azure App Service
4. Habilitar banco de dados
5. Conectar organização Azure DevOps
6. Criar projeto

O Azure DevOps Starter automaticamente:

✔ Cria o repositório Git  
✔ Configura pipeline de Build  
✔ Configura pipeline de Release  
✔ Provisiona Web App e Banco  
✔ Configura Application Insights  

---

# 🔄 Pipeline de CI (Build)

A pipeline de integração contínua executa:

- Checkout do código
- Restore de pacotes NuGet
- Build da aplicação
- Execução de testes
- Publicação de artefato (Drop)

Trigger automático:

```
Commit na branch principal → Nova Build executada
```

A pipeline mantém histórico de versões e permite comparação entre alterações.

---

# 🚀 Pipeline de CD (Release)

A pipeline de release executa:

- Azure Resource Group Deployment
- Azure App Service Deploy
- Azure SQL Database Deployment
- Execução de testes pós-deploy

Deploy contínuo habilitado:

```
Novo artefato gerado → Release automática executada
```

Permite também execução manual quando necessário.

---

# 🧪 Testando o Fluxo CI/CD

Fluxo validado:

1. Alteração no arquivo `Index.cshtml`
2. Commit na branch principal
3. Pipeline de Build executada automaticamente
4. Release disparada
5. Aplicação atualizada no Azure Web App

Resultado:

✔ Deploy automático sem intervenção manual  
✔ Rastreabilidade completa do processo  
✔ Logs detalhados de cada etapa  

---

# 📊 Observabilidade

Monitoramento configurado via:

- Azure Application Insights
- Logs detalhados de build e release
- Histórico de releases
- Auditoria de alterações de pipeline

Possibilidade de visualizar:

- Telemetria da aplicação
- Falhas
- Tempo de resposta
- Dependências

---

# 🔐 Segurança Aplicada

- Controle de acesso via Azure DevOps
- Permissões baseadas em organização
- Deploy via Service Connections seguras
- Separação entre ambiente de build e runtime
- Banco provisionado com credenciais protegidas

---

# 📈 Resultados Técnicos

✔ Pipeline CI/CD totalmente automatizada  
✔ Deploy contínuo funcional  
✔ Provisionamento automático de infraestrutura  
✔ Integração completa com monitoramento  
✔ Modelo pronto para ambientes corporativos  

---

# 📚 Aprendizados Aplicados

- Estruturação de pipeline em Azure DevOps
- Estratégia de CI/CD em aplicações .NET
- Deploy automatizado em Azure App Service
- Integração com banco gerenciado
- Monitoramento com Application Insights
- Governança e rastreabilidade de deploys

---

# ⭐ Se este projeto foi útil

Considere:

- Dar uma estrela ⭐  
- Compartilhar  
- Contribuir com melhorias  

---

> Este projeto demonstra um fluxo completo de CI/CD em Azure para aplicações .NET, simulando um ambiente real de entrega contínua em cloud.
