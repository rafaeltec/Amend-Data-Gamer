# Data History - Dashboard Amend Data Gamer

## Visão Geral
Este documento apresenta o histórico detalhado das etapas realizadas para a criação do dashboard **Amend Data Gamer**, incluindo as atividades, campos calculados, gráficos, design final e estrutura do projeto.

---

## 1. Estrutura do Dashboard
O dashboard foi organizado em **quatro abas principais** para facilitar a navegação e o entendimento do público-alvo:

### **1.1 Página Inicial**
- **Título:** *Amend Data Gamer*
- **Descrição:** Apresenta a divisão do dashboard em seções específicas com botões de navegação.
- **Botões Criados:**
  - **Desempenho de Vendas:** Análises de vendas globais.
  - **Regiões e Produtos:** Dados relacionados a características regionais e produtos vendidos.
  - **Descontos e Logística:** Consolidação de informações sobre logística e descontos.
  - **Agradecimentos:** Reconhecimento pela oportunidade de participar do treinamento e do desafio.

---

## 2. Seção: Desempenho de Vendas
### **Atividades:**
1. **Atividade 2 - Top 10 Clientes por Pedidos em 2016**
   - **Visualização:** Bubble Chart
   - **Campos Calculados:**
     - *Primeiro Nome do Cliente*: `IF FIND([Customer Name], " ") > 0 THEN LEFT([Customer Name], FIND([Customer Name], " ") - 1) ELSE [Customer Name] END`
   - **Insights:** Identifica os 10 principais clientes em termos de número de pedidos realizados.

2. **Atividade 8 - Funcionários com Mais Vendas**
   - **Visualização:** Bubble Chart
   - **Campos Calculados:** Nenhum adicional necessário.
   - **Insights:** Mostra os funcionários responsáveis pelas maiores vendas.

3. **Atividade 1 - Total de Vendas por Categoria**
   - **Visualização:** Barra Horizontal
   - **Campos Calculados:**
     - *Categorias em Português*: `IF [Category] = "Furniture" THEN "Móveis" ELSEIF [Category] = "Technology" THEN "Tecnologia" ELSE "Material de Escritório" END`
   - **Insights:** Apresenta as vendas totais por categorias em todo o período.

4. **Atividade 11 - Lucro ao Longo do Tempo por Modo de Envio**
   - **Visualização:** Gráfico de Linha
   - **Campos Calculados:**
     - *Modo de Envio em Português*: `IF [Ship Mode] = "First Class" THEN "Primeira Classe" ELSEIF [Ship Mode] = "Second Class" THEN "Segunda Classe" ELSEIF [Ship Mode] = "Same Day" THEN "Mesmo Dia" ELSE "Classe Padrão" END`
   - **Insights:** Avalia a evolução do lucro ao longo dos anos para diferentes modos de envio.

---

## 3. Seção: Regiões e Produtos
### **Atividades:**
1. **Atividade 3 - Top 3 Produtos Mais Lucrativos por Região**
   - **Visualização:** Barra Horizontal
   - **Campos Calculados:**
     - *Regiões em Português*: `IF [Region] = "South" THEN "Sul" ELSEIF [Region] = "West" THEN "Oeste" ELSEIF [Region] = "Central" THEN "Central" ELSE "Leste" END`
   - **Insights:** Identifica os produtos mais lucrativos por região.

2. **Atividade 4 - Evolução Trimestral das Vendas na Categoria Mobiliário**
   - **Visualização:** Gráfico de Linha
   - **Campos Calculados:** Nenhum adicional necessário.
   - **Insights:** Exibe o comportamento das vendas trimestrais na categoria mobiliário.

3. **Atividade 6 - Produtos Diferentes Vendidos no Sul**
   - **Visualização:** Mapa com Estados Destacados
   - **Campos Calculados:** Nenhum adicional necessário.
   - **Insights:** Mostra a distribuição de vendas de produtos no Sul dos Estados Unidos.

4. **Atividade 9 - Top 10 Produtos Vendidos no Oeste**
   - **Visualização:** Barra Horizontal
   - **Campos Calculados:** Nenhum adicional necessário.
   - **Insights:** Lista os produtos mais vendidos na região Oeste.

---

## 4. Seção: Descontos e Logística
### **Atividades:**
1. **Atividade 10 - Tempo Médio de Entrega por Região**
   - **Visualização:** Barra Horizontal
   - **Campos Calculados:** Nenhum adicional necessário.
   - **Insights:** Apresenta o tempo médio de entrega por região.

2. **Atividade 5 - Média de Lucro por Pedido em Cada Região**
   - **Visualização:** Barra Horizontal
   - **Campos Calculados:** Nenhum adicional necessário.
   - **Insights:** Avalia a lucratividade média por pedido.

3. **Atividade 7 - Desconto Médio em Pedidos com Prejuízo**
   - **Visualização:** Barra Horizontal
   - **Campos Calculados:**
     - *Categoria de Pedido*: `IF [Profit] < 0 THEN "Prejuízo" ELSE "Lucro" END`
   - **Insights:** Mostra o desconto médio aplicado em pedidos lucrativos e não lucrativos.

---

## 5. Seção: Agradecimentos
- **Descrição:** Página dedicada aos agradecimentos à empresa Amend e aos organizadores do treinamento e desafio.
- **Texto:** "Gostaria de agradecer à Amend e aos organizadores pela oportunidade de aprendizado e prática por meio do treinamento seguido de desafio. Essa abordagem fortalece a integração e o conhecimento colaborativo."

---

## 6. Big Numbers
### Criados para Destaque
1. **Vendas Totais:** `$2.297.201`
2. **Total de Pedidos:** `4.587`
3. **Lucro Total:** `$895.452`

---

## 7. Considerações Finais
- Este dashboard foi estruturado para oferecer **insights estratégicos e operacionais**, atendendo aos objetivos propostos no desafio.
- Cada seção e gráfico foi pensado para **clareza visual** e **efetividade de análise**.

---

**Amend Data Gamer Dashboard - 2024**
