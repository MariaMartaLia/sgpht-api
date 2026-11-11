# 🥬 SGPHT — Sistema de Gestão e PDV para Hortifruti

<p align="left">
  <img src="https://jsdelivr.net" width="48" height="48" alt="Java 21" title="Java 21" />
  &nbsp;&nbsp;
  <img src="https://jsdelivr.net" width="48" height="48" alt="Spring Boot 3" title="Spring Boot 3" />
  &nbsp;&nbsp;
  <img src="https://jsdelivr.net" width="48" height="48" alt="PostgreSQL" title="PostgreSQL" />
</p>


> **Status do Projeto:** 📝 Em fase de planejamento e estruturação inicial

## 💡 1. Visão Geral e Problema Resolvido

Gerenciar um hortifruti exige agilidade e precisão extrema. A operação lida diariamente com **produtos altamente perecíveis** e **vendas fracionadas por peso**, onde pequenos erros de cálculo ou falhas na baixa de estoque geram prejuízo financeiro direto no caixa.

Este projeto é uma solução de Backend robusta desenvolvida para resolver essa dor. O objetivo do sistema é garantir consistência rigorosa no controle de estoque, automatizar vendas por quilo ou unidade, rastrear perdas estruturais (descartes) e gerar inteligência de negócios através de relatórios analíticos de progresso e regresso.

---

## 🛠️ 2. Arquitetura e Tecnologias Planejadas

Cada tecnologia foi escolhida com foco em integridade financeira, segurança de dados e boas práticas de engenharia de software:

* **Java 21 & Spring Boot 3.x:** Base moderna e escalável para a construção da API RESTful.
* **PostgreSQL:** Banco de dados relacional escolhido para garantir **transações ACID rígidas**, evitando qualquer inconsistência ou perda de dados durante a baixa simultânea de estoque.
* **Precisão Numérica (`BigDecimal`):** Uso obrigatório da classe `BigDecimal` para valores monetários e pesos fracionados, eliminando falhas de arredondamento de ponto flutuante.
* **Arquitetura em Camadas:** Organização limpa dividida em `Controller`, `Service`, `Repository` e `Domain/Entity` para facilitar a manutenção e a criação de testes.

---

## 📋 3. Escopo e Requisitos Funcionais (RF)

### 📦 Gestão de Produtos e Estoque
* **[RF001] Cadastro de Produtos:** Registro com Nome, Categoria, Preço Base e Status (`Ativo`/`Inativo`), suportando precificação **Por Unidade** (inteiros) e **Por Peso/Quilo** (decimais).
* **[RF002] Fluxo de Entrada de Estoque:** Registro de compras associando o custo de aquisição e a quantidade adquirida (em kg ou unidades).
* **[RF004] Registro de Perdas (Descarte):** Baixa manual no estoque para itens estragados ou vencidos, categorizando o motivo da perda.

### 🛒 Frente de Caixa (PDV)
* **[RF003] Fluxo de Saída e Venda:** Abertura de pedidos com cálculo dinâmico do subtotal com base no peso/quantidade (Ex: `0.350 kg × R$ 8,00`) e baixa automática e atômica no estoque após confirmação.

### 📊 Relatórios e Inteligência de Negócios
* **[RF005] Relatórios Diários:** Fechamento consolidando total faturado, quantidade de itens vendidos e impacto financeiro/quantitativo das perdas.
* **[RF006] Relatório Mensal de Progresso/Regresso:** Comparativo histórico dos últimos meses analisando o crescimento das vendas versus a variação no índice de desperdício.

---

## 🗺️ 4. Roadmap de Desenvolvimento

Acompanhe a evolução da construção do sistema:

- [x] Definição de escopo, regras de negócio e arquitetura
- [ ] Modelagem do banco de dados relacional (DER)
- [ ] Criação do projeto base com Spring Boot e conexão com PostgreSQL
- [ ] Implementação do cadastro de produtos e entrada de estoque (`RF001` e `RF002`)
- [ ] Implementação do módulo de PDV e vendas fracionadas (`RF003`)
- [ ] Implementação do controle de perdas e relatórios analíticos (`RF004`, `RF005` e `RF006`)
- [ ] Documentação dos endpoints e testes automatizados

---

## 👩‍💻 Autoria

Desenvolvido por **Maria Marta Almeida Brito**  
*Graduanda em Análise e Desenvolvimento de Sistemas*  

<p align="left">
  <a href="https://linkedin.com" target="_blank">
    <img src="https://jsdelivr.net" width="36" height="36" alt="LinkedIn" title="Conectar no LinkedIn" />
  </a>
  &nbsp;&nbsp;
  <a href="https://github.com" target="_blank">
    <img src="https://jsdelivr.net" width="36" height="36" alt="GitHub" title="Ver GitHub" />
  </a>
</p>


