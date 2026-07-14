# 📦 Olist: Expectativa vs. Realidade Logística no E-commerce

Uma análise baseada no dataset Olist (Kaggle), explorando 9 tabelas via banco de dados relacional para investigar o que realmente impacta a satisfação do cliente.

### ❓ A Pergunta de Negócio
Com 11 mil pedidos recebendo a avaliação mínima (nota 1), o que realmente irrita mais o cliente: a lentidão absoluta da entrega ou a quebra da expectativa do prazo prometido?

### 📊 A Descoberta
Ao classificar os pedidos comparando a entrega real com a data estipulada, os números revelaram um impacto brutal:
* **92%** dos pedidos chegam adiantados, resultando em uma nota média excelente de **4,29**.
* **8%** dos pedidos sofrem atraso, fazendo a nota média despencar para **2,57** (uma queda imediata de 40,1% na avaliação).

### 💡 A Tese
A satisfação no e-commerce é estritamente sobre **gestão de expectativa, e não velocidade**. Os dados provam que um cliente do Amapá (que espera 27 dias pelo produto) avalia a loja com a nota praticamente igual (4,242 contra 4,246) à de um cliente de São Paulo (que espera apenas 9 dias). A recomendação de negócio é clara: o foco não deve ser apenas entregar mais rápido, mas ajustar a promessa e cumprir os prazos estabelecidos.

### ⚙️ Ferramentas Utilizadas
* **Linguagens:** SQL (SQLite) e Python (pandas).
* **Ambiente:** Google Colab.

### 🛠️ Destaque Técnico (Qualidade de Dados)
Durante a auditoria da base, identifiquei uma inconsistência: 547 pedidos possuíam avaliações duplicadas devido a rotinas de entregas fracionadas. Para proteger a qualidade da análise, tratei esse ruído criando a CTE `reviews_unicas`, que consolidou as notas via média aritmética antes dos cruzamentos principais, garantindo a total robustez dos achados.

### 📈 Prazos vs. Satisfação por Estado
> *O gráfico abaixo demonstra a correlação entre os dias de adiantamento da entrega e a média de avaliação dos clientes em cada UF.*

![Gráfico Scatter Olist]<img width="576" height="433" alt="image" src="https://github.com/user-attachments/assets/e0958ca8-aaa6-4746-8f65-9cb480bb6c44" />


-
