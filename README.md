# 💰 Detector de Golpe Pix - Sistema Antifraude

Este é um projeto Java que simula um sistema antifraude para detectar possíveis golpes via Pix, com foco em conscientizar e auxiliar vítimas. Ele oferece um sistema simples para entrada de dados de transações e, em caso de detecção de golpe, orienta o usuário e registra as informações da vítima em um banco de dados local.

---

## 🚀 Requisitos Funcionais

| Identificador | Requisito Funcional               | Descrição                                                                                                                                              |
|---------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| RF01          | Informar Dados de Transação       | O usuário pode informar o remetente, valor e a mensagem de uma transação Pix                                                                           |
| RF02          | Detectar Golpes                   | Análise da mensagem de transação para identificar padrões que podem indicar um golpe (ex.: "presente", "frete", "pagamento")                           |
| RF03          | Confirmar Pagamento               | Após a detecção de um possível golpe, o sistema pergunta se o usuário efetuou o pagamento                                                              |
| RF04          | Coletar Dados da Vítima           | Se o golpe for confirmado e o pagamento realizado, o sistema exibe um alerta e coleta informações da vítima (nome, CPF, banco)                         |
| RF05          | Registrar Vítimas                 | As informações das vítimas são armazenadas em um banco de dados SQLite local                                                                           |
| RF06          | Realizar Boletim de Ocorrência    | Oferece a opção de abrir o link da Delegacia Eletrônica da Polícia Civil de SP para registro de boletim de ocorrência                                  |

---

## Requisitos NÃO Funcionais

| Identificador | Requisito Não Funcional         | Descrição                                                                                                                                                           |
|---------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RNF01         | Usabilidade                     | Interface amigável com telas claras e objetivas; fluxo intuitivo com validação em tempo real e mensagens informativas (ex.: "valor inválido", "dados obrigatórios") |
| RNF02         | Segurança                       | Criptografia de dados sensíveis (CPF, nome, transações); registro de auditoria com logs legíveis e timestamp                                                        |
| RNF03         | Confiabilidade & Resiliência    | Persistência segura usando transações em banco de dados (ex.: SQLite) para evitar inconsistências                                                                  |
| RNF04         | Desempenho                      | Interações básicas devem responder em menos de 200 ms em média durante navegação comum                                                                              |
| RNF05         | Manutenção & Evolução           | Cobertura de testes automatizados (> 80%) para regras de detecção de fraudes e persistência de dados                                                              |
| RNF06         | Privacidade & Conformidade      | Armazenar apenas dados sensíveis estritamente necessários, com aviso ao usuário                                                                                     |

---

## 🛠️ Tecnologias Utilizadas

* **Java 21**
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

1. Ter as ferramentas listadas instaladas no seu computador:
   - **IDE Java**
     - Utilizada no projeto: **NetBeans**
   - **Banco de dados**
     - Utilizado no projeto: **DB Browser for SQLite**

2. Baixar e descompactar o projeto deste repositório para seu computador.

3. Garantir que esteja instalado no projeto o driver `mysql-connector-j-####.jar` para conexão com o banco de dados.

4. Garantir que a biblioteca `sqlite-jdbc` esteja instalada.

5. A versão do JDK Java deve estar atualizada.

6. Garantir que a base de dados seja importada automaticamente; caso não tenha sido, importar manualmente.

7. Executar o projeto.


---

## Diagrama de Classe

<div align="center">
<img src="https://i.ibb.co/WNsNYWwx/Captura-de-tela-2025-06-10-192908.png" width="600">
</div>

---

## Diagrama de Caso de Uso

<div align="center">
<img src="https://i.ibb.co/Q3gL84HB/Whats-App-Image-2025-06-13-at-21-08-42.jpg" width="600">
</div>

---

## Modelo de Entidade e Relacionamento (MER)

<div align="center">
  <img src="https://github.com/user-attachments/assets/5d8611ac-563e-448f-bf95-eee486de10ad" width="600">
</div>

---

## Colaboradores

| <a href="https://github.com/andressamartinss"><img src="https://avatars.githubusercontent.com/u/124886469?v=4" width="200px" alt="Andressa Martins"></a> | <a href="https://github.com/JFF27"><img src="https://avatars.githubusercontent.com/u/186189173?v=4" width="200px" alt="Júlia Ferreira"></a> | <a href="https://github.com/Akemyk"><img src="https://avatars.githubusercontent.com/u/144185022?v=4" width="200px" alt="Júlia Kitano"></a> | <a href="https://github.com/silva2ma"><img src="https://avatars.githubusercontent.com/u/162327871?v=4" width="200px" alt="Marcela Rodrigues"></a> | <a href="https://github.com/MatheusGoncalvx"><img src="https://avatars.githubusercontent.com/u/126586389?v=4" width="200px" alt="Matheus Gonçalves"></a> | <a href="https://github.com/Nick-O-Hara"><img src="https://avatars.githubusercontent.com/u/204797509?v=4" width="200px" alt="Nicolas"></a> | <a href="https://github.com/AqueleQueEspera"><img src="https://avatars.githubusercontent.com/u/214915153?v=4" width="200px" alt="Sandro Campos"></a> |
| --- | --- | --- | --- | --- | --- | --- |
| Andressa Martins | Júlia Ferreira | Júlia Kitano | Marcela Rodrigues | Matheus Gonçalves | Nicolas Conceição | Sandro Campos |
