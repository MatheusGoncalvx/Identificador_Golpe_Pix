# 💰 Detector de Golpe Pix - Sistema Antifraude

Este é um projeto Java que simula um sistema antifraude para detectar possíveis golpes via Pix, com foco em conscientizar e auxiliar vítimas. Ele oferece um sistema simples para entrada de dados de transações e, em caso de detecção de golpe, orienta o usuário e registra as informações da vítima em um banco de dados local.

---

## 🚀 Funcionalidades

* **Entrada de Dados de Transação:** O usuário pode informar o remetente, valor e a mensagem de uma transação Pix.
* **Detecção de Golpes:** Análise da mensagem da transação para identificar padrões que podem indicar um golpe (ex: "presente", "frete", "pagamento").
* **Confirmação de Pagamento:** Após a detecção de um possível golpe, o sistema pergunta se o usuário efetuou o pagamento.
* **Alerta e Coleta de Dados da Vítima:** Se o golpe for confirmado e o pagamento realizado, o sistema exibe um alerta e coleta informações da vítima (nome, CPF, banco).
* **Registro de Vítimas:** As informações das vítimas são armazenadas em um banco de dados SQLite local.
* **Boletim de Ocorrência Online:** Oferece a opção de abrir o link da Delegacia Eletrônica da Polícia Civil de SP para registro de boletim de ocorrência.

---

## 🛠️ Tecnologias Utilizadas

* **Java**
* **SQLite JDBC:** Para conexão e manipulação do banco de dados SQLite.

---

## 📁 Estrutura do Projeto

O projeto está organizado nas seguintes classes e pacotes:

* `a3_golpedopix/`
    * **`DetectorGolpePix.java`:** Classe principal que inicia a aplicação, coleta dados e orquestra o fluxo de detecção.
    * **`DetectorGolpePix.java`:** Classe principal que inicia a aplicação, coleta dados e orquestra o fluxo de detecção.
    * **`TransacaoPix.java`:** Representa uma transação Pix e contém a lógica inicial de verificação de golpes.
    * **`PresenteSuspeito.java`:** Estende `TransacaoPix`, lida com a lógica pós-detecção de golpe (coleta de dados da vítima, alerta e BO).
    * **`TipoGolpe.java`:** Enumeração que define os tipos de golpes que podem ser registrados.
    * **`Vitima.java`:** Classe de modelo que representa uma vítima de golpe.
    * **`VitimaDAO.java`:** Camada de acesso a dados para a entidade `Vitima`, responsável pelas operações de CRUD no banco.
    * **`ConexaoBD.java`:** (Assumida) Classe responsável por estabelecer a conexão com o banco de dados SQLite.
---

## ▶️ Como Rodar o Projeto

...

---

## Diagrama de Classe do Projeto

...

---

## Diagrama de Caso de Uso

...

---
-
