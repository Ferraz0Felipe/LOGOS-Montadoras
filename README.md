# KATA PORTAL - Gestão de Estratégias e Desafios

O **KATA PORTAL** é uma aplicação web baseada no ecossistema Google, projetada para gerenciar o progresso de desafios (Katas), monitorar o sentimento do cliente e traçar estratégias para diferentes montadoras do setor automotivo. A ferramenta centraliza informações de progresso, obstáculos e próximos passos em uma interface moderna e intuitiva.

## 🚀 Começando

Essas instruções permitirão que você obtenha uma cópia do projeto em operação na sua conta Google para fins de desenvolvimento e uso administrativo.

Consulte **[Implantação](#-implanta%C3%A7%C3%A3o)** para saber como publicar o projeto como um Web App.

### 📋 Pré-requisitos

Para utilizar este projeto, você precisará de:
* Uma conta Google (Gmail ou Google Workspace).
* Acesso ao Google Drive.
* Uma planilha do Google Sheets para servir como banco de dados.

### 🔧 Instalação

Siga o passo-a-passo abaixo para configurar o ambiente:

1.  **Criar a Planilha:**
    Crie uma nova planilha no Google Sheets e anote o seu `ID` (presente na URL entre `/d/` e `/edit`).

2.  **Configurar o Google Apps Script:**
    Na planilha, vá em `Extensões` > `Apps Script`.

3.  **Adicionar o Código Backend:**
    Crie um arquivo chamado `Código.gs` e cole o código JavaScript do lado do servidor (as funções `doGet`, `salvarCartao`, `listarCartoes`, etc.). Certifique-se de atualizar o `SPREADSHEET_ID` no objeto `CONFIG`.

4.  **Adicionar a Interface Frontend:**
    No editor do Apps Script, clique no ícone `+` e selecione `HTML`. Nomeie o arquivo como `Interface`. Cole todo o código HTML/CSS/JS da interface.

5.  **Configurar Cabeçalhos (Opcional):**
    O script criará automaticamente a aba "Gestao_Kata" e os cabeçalhos na primeira execução.

---
**Demonstração de uso:**
Ao abrir o link gerado, selecione a montadora (ex: VW), digite o desafio, selecione o emoji de sentimento e registre. O card aparecerá instantaneamente na aba "Em Andamento".

## ⚙️ Executando os testes

Os testes deste sistema são realizados verificando a comunicação entre o formulário HTML e a planilha Google.

### 🔩 Analise os testes de ponta a ponta

Para validar o fluxo de dados:
1.  **Teste de Escrita:** Insira dados no formulário e clique em "Registrar Kata". Verifique se uma nova linha apareceu na planilha Google Sheets.
2.  **Teste de Leitura:** Navegue até "Em Andamento" e confirme se os dados exibidos nos cards correspondem exatamente ao que está na planilha.

### ⌨️ Testes de estilo e responsividade

Verifique se o layout se adapta corretamente:
1.  Redimensione a janela do navegador para garantir que o `grid` de cartões se ajuste (responsividade).
2.  Verifique se o cálculo de "dias" no topo do card está correto em relação à data de criação na planilha.

## 📦 Implantação

Para implantar o sistema em produção:
1.  No editor do Apps Script, clique em **Implantar** > **Nova Implantação**.
2.  Selecione o tipo **App da Web**.
3.  Configure "Executar como" para **Você** e "Quem tem acesso" para **Qualquer pessoa com conta Google** (ou conforme sua necessidade).
4.  Copie a URL fornecida; este é o seu link de acesso ao Portal.

## 🛠️ Construído com

* [Google Apps Script](https://developers.google.com/apps-script) - O framework de backend e hospedagem.
* [Google Sheets](https://www.google.com/sheets/about/) - O banco de dados para armazenamento de registros.
* [JavaScript/HTML5/CSS3](https://developer.mozilla.org/pt-BR/) - Tecnologias utilizadas para a interface e lógica do cliente.

## 📌 Versão

Nós usamos [SemVer](http://semver.org/) para controle de versão. Atualmente o projeto encontra-se na versão **1.2.0** (Ajustes de layout e visualização de estratégia).

## ✒️ Autores

* **Felipe Ferraz** - *Desenvolvimento Inicial e Design* - [Ferraz0Felipe](https://github.com/Ferraz0Felipe)

## 📄 Licença

Este projeto está sob a licença MIT - consulte o arquivo LICENSE.md para detalhes.

## 🎁 Expressões de gratidão

* Projeto desenvolvido para otimizar o acompanhamento de melhoria contínua 📈.
* Um agradecimento a todos que utilizam o Kata para transformar desafios em resultados 🚀.

---
⌨️ com ❤️ por [Felipe Ferraz](https://github.com/Ferraz0Felipe) 😊
