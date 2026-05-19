# 📍 RotaSolidária

> **Projeto Temático A3** - Desenvolvimento de Sistemas Desktop com Integração de Banco de Dados.
> Curso de Tecnologia / Engenharia - Faculdade [Nome da sua Faculdade].

---

## 🎯 Sobre o Projeto

O **RotaSolidária** é uma aplicação desktop em Java desenvolvida para mitigar a superlotação e as longas filas de espera nos postos de atendimento do CadÚnico. O sistema atua como um roteador inteligente de assistência social, com foco especial no acolhimento e direcionamento rápido de **refugiados e pessoas em situação de vulnerabilidade**.

A aplicação cruza as necessidades e a localização do solicitante para indicar em tempo real o posto de atendimento mais próximo, com maior disponibilidade e menor tempo de espera.

---

## 💻 Funcionalidades Principais

* **Cadastro Simplificado (Solicitante):** Formulário adaptado para refugiados (aceita Passaporte/RNE além do CPF) e suporte inicial a múltiplos idiomas.
* **Triagem de Necessidades:** Filtro por demandas urgentes (Documentação, Alimentação, Abrigo).
* **Roteamento Inteligente:** Algoritmo no Back-end que calcula e sugere o posto com menor fila na região do usuário.
* **Painel Administrativo (Posto):** Interface para que os funcionários do CadÚnico atualizem o status de lotação do local em tempo real (Disponível, Moderado, Lotado).

---

## 🧱 Arquitetura e Estrutura do Projeto

O desenvolvimento do projeto seguiu uma abordagem híbrida de ferramentas para extrair o melhor de cada ecossistema:
* **NetBeans (Interface Visual):** Utilizado exclusivamente como construtor gráfico (GUI Builder / Swing) para desenho rápido e responsivo das telas.
* **VS Code (Back-end e Regras de Negócio):** Utilizado como ambiente de desenvolvimento principal para a codificação da lógica em Java, tratamento de eventos e persistência de dados.

O código foi estruturado utilizando o padrão de arquitetura **MVC (Model-View-Controller)** e o padrão **DAO (Data Access Object)** para isolar as consultas SQL da interface gráfica.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Java 17 (ou a versão que vocês estiverem usando)
* **Interface Gráfica:** Java Swing / AWT
* **Banco de Dados:** MySQL (SGBD Relacional)
* **Biblioteca de Conexão:** JDBC (Java Database Connectivity) + Driver MySQL Connector/J

---

## 💾 Modelagem do Banco de Dados (Estrutura Inicial)

O banco de dados `db_rotasolidaria` é composto pelas seguintes entidades relacionais:

* `tb_usuarios`: Armazena dados dos cidadãos/refugiados solicitantes.
* `tb_postos_atendimento`: Armazena o endereço, capacidade e índice de lotação de cada posto CadÚnico.
* `tb_encaminhamentos`: Tabela pivô que registra os protocolos gerados e vincula o usuário ao posto recomendado.
