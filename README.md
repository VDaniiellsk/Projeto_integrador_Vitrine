# Vitrine Digital - Fortalecimento e Resiliência da Mão de Obra Local

> **tecnologia social de código aberto desenvolvida como Projeto Integrador para o programa de extensão UFMS Digital.**
> O ecossistema conecta diretamente prestadores de serviços autônomos a tomadores de demanda no Bairro da Paz (Salvador-BA), mitigando a assimetria de informação e a exclusão digital de segunda ordem.

---

## 📌 Contexto e Justificativa

No cenário urbano periférico, o avanço do capitalismo de plataforma impõe barreiras de entrada e taxas predatórias que asfixiam a autonomia de trabalhadores informais. A **Vitrine Digital** surge como um contraponto ético baseado nos princípios do **Cooperativismo de Plataforma** (Trebor Scholz).

O direcionamento da arquitetura de software foi guiado por dados estatísticos reais coletados em campo com 41 respondentes da comunidade:
* **31,7%** dos usuários sofrem cronicamente com escassez de armazenamento e memória cheia nos celulares.
* **43,9%** dependem exclusivamente de pacotes limitados de dados móveis (3G/4G/5G) na rua.
* **87,8%** preferem contratar profissionais do próprio bairro, mas enfrentam barreiras de confiança e medo latente de golpes digitais.

---

## 🏗️ Solução Tecnológica e Arquitetura

Para contornar as severas restrições de hardware e conectividade, foi descartada a ideia inicial de um aplicativo nativo. A solução final foi projetada como um **Progressive Web App (PWA)** responsivo e *mobile-first*:

1. **Acessibilidade Cognitiva Extrema:** Sem fluxos burocráticos de login, e-mails ou senhas complexas para os clientes. Busca direta baseada em filtros de ofício e georreferenciamento simples.
2. **Potencialização do "Boca a Boca" (Apelo Cultural):** O sistema digitaliza e confere escala aos laços de confiança locais posicionando o mural de **Avaliações Comunitárias** (notas e comentários de vizinhos) no topo do perfil do prestador.
3. **Retenção de Renda Integral:** Conexão final integrada diretamente à API do WhatsApp por meio de um botão de clique único. O trabalhador mantém 100% dos seus ganhos, livre de taxas de intermediação.

---

## 📊 Engenharia de Software e Modelagem

O projeto foi modelado utilizando o software **Astah**, garantindo a transição da persistência lógica para o paradigma orientado a objetos.


### 🗃️ Modelo Relacional do Banco de Dados (DER)
A persistência de dados foi estruturada de forma enxuta, utilizando chaves primárias ($PK$) e chaves estrangeiras ($FK$) referenciais, eliminando tabelas desnecessárias de clientes:

* `PRESTADORES`: Centraliza dados cadastrais e profissionais públicos do autônomo.
* `CATEGORIAS_SERVICO`: Gerencia a indexação e os filtros macro de ofícios na interface.
* `SERVICOS_PRESTADOR`: **Classe de Associação** que quebra o relacionamento muitos-para-muitos ($N:M$), vinculando o profissional ao seu preço-hora (`decimal`).
* `PORTFOLIO_FOTOS`: Controla o limite de mídias para compressão assíncrona automatizada no servidor.
* `AVALIACOES_COMUNITARIAS`: Armazena depoimentos e notas de forma declarativa, resguardando o anonimato do cliente por meio de campos puramente textuais.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

* **Prototipagem de Interface:** Figma (Alta Fidelidade)
* **Modelagem de Sistemas e UML:** Astah Professional (Diagramas de Caso de Uso, Classes, Sequência e DER)
* **Modelagem Conceitual:** Coggle
* **Documentação Científica:** Google Docs (Padrão ABNT NBR 6023:2018)

---

## 📚 Referencial Teórico Base

* **DIJK, Jan van.** *The Deepening Divide: Inequality in the Information Society.* (Exclusão digital de segunda ordem).
* **SCHOLZ, Trebor.** *Cooperativismo de plataforma: contestando a economia do compartilhamento corporativa.*
* **BOURDIEU, Pierre.** *A distinção: crítica social do julgamento.* (Capital Social).
* **GRANOVETTER, Mark.** *The Strength of Weak Ties.* (A força dos laços fracos).

---
Developed by **Vitor Daniel Dos Santos Alves** *Academic Student of Information Technology - UFMS Digital (2026.1)*
