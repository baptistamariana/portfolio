<h1 align="center"> FICA FRIO </h1>

![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)
![Tecnologia](https://img.shields.io/badge/Feito%20com-C%23%20-blue)
![Licença](https://img.shields.io/badge/Licen%C3%A7a-Acad%C3%AAmica-lightgrey)

**Curso:** Análise e Desenvolvimento de Sistemas  
**Projeto:** Desenvolvimento de uma Aplicação Interativa  
**Período:** 2º Semestre  
**Tecnologias principais:** C# | ASP.NET MVC | HTML | CSS | JavaScript

## 📌 Sobre o Projeto

**Fica Frio** é uma plataforma digital que utiliza **geolocalização** para mapear **pontos de água potável gratuitos** na cidade. Usuários podem visualizar os pontos em um mapa interativo, avaliar a qualidade da água, sugerir novos locais e manter os dados atualizados.

A iniciativa promove o acesso à água potável, estimula a sustentabilidade urbana e fortalece a colaboração comunitária ao reduzir o uso de garrafas plásticas descartáveis.

### 🔹 Funcionalidades principais:

- Cadastro de usuários
- Avaliação e comentários sobre a qualidade da água
- Sugestão de novos pontos de água
- Atualização de informações por responsáveis dos pontos

O sistema promove o **acesso fácil à água potável**, incentiva a **hidratação consciente**, **reduz o uso de garrafas plásticas** e **fortalece a colaboração comunitária**.


## 👥 Integrantes

- Alice Maria Beteli Zanon Alonso  
- Gustavo Felix Correia  
- João Vítor Alves de Mello Costa  
- Leopoldo Pereira da Fonseca  
- Mariana Santos Baptista  
- Maria Eduarda Microni Quites Ferreira  

**Orientador:** Bernardo Jeunon de Alencar

## 🚀 Como Executar o Projeto Localmente

### 📥 Pré-requisitos

- [.NET SDK 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) instalado  
- Visual Studio 2022 (ou superior) ou VS Code com extensão C#  
- SQL Server local (SQL Server Express, Docker ou outra instância)  
- Git instalado

### 🔧 Passos

### 1. Faça um push para a branch `main`

Sempre que você der um `push` para a branch `main`, o GitHub Actions executará automaticamente o pipeline de CI/CD, que irá:

- Restaurar as dependências do projeto
- Construir o projeto ASP.NET Core
- Executar as Migrations do Entity Framework no banco Azure SQL
- Publicar a aplicação na Azure Web App

---

### 2. Configure os segredos do GitHub (GitHub Secrets)

Para que o workflow funcione corretamente, você precisa configurar dois secrets no repositório:

| Nome do segredo | Descrição |
|-----------------|-----------|
| `AZURE_SQL_CONNECTION_STRING` | String de conexão completa do banco de dados Azure SQL |
| `AZUREAPPSERVICE_PUBLISHPROFILE_CDC4E7E12F37428EAF1B2F9F5BF71D8A` | Publish Profile da sua Azure Web App (obtido no portal da Azure) |

#### 📌 Como adicionar:
- Acesse seu repositório no GitHub
- Vá em **Settings** → **Secrets and variables** → **Actions**
- Clique em **New repository secret**
- Cole os valores corretamente

---

### 3. Estrutura dos diretórios utilizados

Seu projeto está estruturado assim:

```
src/
└── FicaFrio/
    └── FicaFrio/
        ├── FicaFrio.csproj
        ├── appsettings.json
        └── ...
```

---

### 4. Execução local (opcional)

Se quiser rodar o projeto localmente antes de enviar para produção:

```bash
# Restaura dependências
dotnet restore src/FicaFrio/FicaFrio/FicaFrio.csproj

# Aplica migrations (local)
dotnet ef database update --project src/FicaFrio/FicaFrio/FicaFrio.csproj

# Roda o projeto
dotnet run --project src/FicaFrio/FicaFrio/FicaFrio.csproj
```

---

### 5. Acesse sua aplicação

Após o deploy, sua aplicação estará disponível no endereço configurado na Azure Web App:

```plaintext
https://ficafrio.azurewebsites.net
```


