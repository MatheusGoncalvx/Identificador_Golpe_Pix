# 💰 Detector de Golpe Pix - Sistema Antifraude

Este é um projeto Java que simula um sistema antifraude para detectar possíveis golpes via Pix, com foco em conscientizar e auxiliar vítimas. Ele oferece um sistema simples para entrada de dados de transações e, em caso de detecção de golpe, orienta o usuário e registra as informações da vítima em um banco de dados local.

---

## 🚀 Funcionalidades

* **Entrada de Dados de Transação:** O usuário pode informar o remetente, valor e a mensagem de uma transação Pix.

---

## 🛠️ Tecnologias Utilizadas

* **Java**
* **SQLite JDBC:** Para conexão e manipulação do banco de dados SQLite.

---

## 📁 Estrutura do Projeto

O projeto está organizado nas seguintes classes e pacotes:

* `a3_golpedopix/`
    * **`DetectorGolpePix.java`:** Classe principal que inicia a aplicação, coleta dados e orquestra o fluxo de detecção.
    ...
---

## ▶️ Como Rodar o Projeto

1.  **Clone o Repositório:**
    ```bash
    
    ```
2.  **Abra em uma IDE:** Importe o projeto em sua IDE Java favorita (IntelliJ IDEA, Eclipse, NetBeans).
3.  **Adicione a Dependência SQLite JDBC:**
    * **Maven/Gradle:** Se estiver usando, adicione a dependência `org.xerial:sqlite-jdbc` ao seu `pom.xml` ou `build.gradle`.
    * **Manual (para IDEs):** Baixe o JAR do driver SQLite JDBC (você pode encontrar a versão mais recente em [MVNRepository - SQLite JDBC](https://mvnrepository.com/artifact/org.xerial/sqlite-jdbc)) e adicione-o ao `classpath` do seu projeto.
4.  **Execute a Classe Principal:** Execute a classe `DetectorGolpePix.java`.

O sistema iniciará com uma janela de diálogo para entrada de informações.
