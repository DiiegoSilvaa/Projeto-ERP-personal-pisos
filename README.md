# Projeto ERP — Personal Pisos

## 1. Identificação da equipe
* Bruna Soares de Almeida - RGM: 47552158
* Caua Hernandes Honorato - RGM: 47863617
* Diego Silva - RGM: 47855533
* Esther Mari de Souza - RGM: 47487135
* Felipe Dyonisio da Silva Veiga - RGM: 45698732
* Guilherme de Aquino Campos - RGM: 48183939
* Julia Lafaelly Frazão Nunes - RGM: 48127507
* Marcos Murilo Fernandes da Silva - RGM: 48159786

---

## 2. Caracterização da empresa
* **Nome:** Personal Pisos
* **Segmento:** Design de Interiores e Acabamentos.
* **O que vende:** Soluções completas para ambientação, indo desde revestimentos de piso (vinílicos, laminados, porcelanatos) e proteção solar (persianas, cortinas sob medida) até elementos de decoração geral (papel de parede, tapetes, painéis).
* **Principais Clientes:** Pessoas físicas reformando ou construindo a casa própria, arquitetos/designers de interiores parceiros e pequenos construtores.
* **Setores:** Marketing, Vendas, Gerência, Finanças e Contabilidade, RH e Logística/Instalação.
* **Funcionamento Operacional:** Modelo de negócio híbrido (digital e showroom físico).
* **Dados:** Dados do Cliente, Dados Logísticos, Dados Técnicos e Dados Financeiros.

---

## 3. Justificativa da escolha
O grupo escolheu a empresa porque ela já possui um site que precisa de melhorias estruturais e da implementação de um banco de dados organizado para gerenciar suas informações. Além disso, há facilidade de acesso aos processos reais, pois uma das integrantes atua diretamente na empresa.

---

## 4. Problemas e necessidades identificados
* **Problema:** Problemas não identificados durante a visita técnica pré-obra.  
  *Consequência:* Retrabalho durante a instalação ou execução do serviço.
* **Problema:** Processos de administração ou venda não seguidos corretamente.  
  *Consequência:* Retrabalho e possíveis atrasos nos processos.
* **Problema:** Informações duplicadas durante a reestruturação do sistema.  
  *Consequência:* Necessidade de reorganização e conferência dos dados.
* **Problema:** Possibilidade de perda de informações.  
  *Consequência:* Dificuldade para manter todos os dados organizados e disponíveis.
* **Problema:** Uso de planilhas junto aos sistemas.  
  *Consequência:* Necessidade de modernização e integração dos controles.
* **Problema:** Controle de estoque sem colaborador específico.  
  *Consequência:* Maior dificuldade e trabalho para acompanhar o estoque.
* **Problema:** Informações dependentes de cadastro correto.  
  *Consequência:* Possibilidade de dificuldades no acompanhamento quando há falhas no cadastro.

---

## 5. Processos de negócio
* **Fluxo Geral:** Cliente -> Solicita orçamento -> Projeto -> Agendamento de visita -> Medição -> Compra de produtos -> Pagamento -> Entrega -> Montagem/Instalação -> Atualização do estoque.
* **Participantes:** Cliente, vendedor, designer de interiores, montador e financeiro.
* **Gatilho Inicial:** O cliente solicita um orçamento ou procura um produto específico.
* **Informações Geradas:** Orçamento, medidas do ambiente, pedido de venda, produtos vendidos, nota fiscal, comprovante de pagamento e atualização do estoque.

---

## 6. Requisitos funcionais
* **RF1:** O sistema deve permitir o cadastro de dados pessoais do cliente (E-mail, celular, Nome completo, CPF/CNPJ, Data de nascimento e CEP) com verificação em duas etapas.
* **RF2:** O sistema deve permitir a emissão de relatórios.
* **RF3:** O sistema deve prover um canal de contato direto entre cliente e atendente.
* **RF4:** O sistema deve permitir o controle de estoque.
* **RF5:** O sistema deve permitir a criação de orçamentos prévios de serviço, com validade configurável (ex: 7 dias).
* **RF6:** O sistema deve permitir especificar o estilo de decoração desejado.
* **RF7:** O sistema deve registrar todo o processo, desde a compra do material até a sua venda final.
* **RF8:** O sistema deve registrar quais produtos estão disponíveis para venda.
* **RF9:** O sistema deve calcular o valor total da venda considerando a quantidade de serviços e materiais.

---

## 7. Requisitos não funcionais
* **RNF1:** O sistema deve realizar backup diário automático dos dados.
* **RNF2:** O sistema deve responder às requisições do usuário em tempo hábil (meta de até 0,5 segundos por clique).
* **RNF3:** O sistema deve manter alta disponibilidade (24 horas por dia, 7 dias por semana).
* **RNF4:** O sistema deve possuir interface responsiva (compatível com dispositivos móveis e desktops).
* **RNF5:** O sistema deve estar em conformidade com as diretrizes da LGPD, garantindo o controle de acesso e sigilo das informações dos clientes.

---

## 8. Regras de negócio
* **RN1:** Um mesmo lote/material específico alocado a um pedido não pode ser vendido para mais de um cliente.
* **RN2:** O pagamento parcelado exige um sinal de 35% do valor total da compra.
* **RN3:** O cálculo total do pedido deve somar o valor do material, custos de fornecedores, metragem quadrada e valor da instalação.
* **RN4:** O cancelamento com reembolso total é permitido até 7 dias antes do início da obra/instalação.

---

## 9. Restrições e políticas organizacionais
* **Aprovações Operacionais:** Apenas Gerentes/Proprietários podem autorizar descontos superiores a 5%, exclusões de dados e métodos especiais de pagamento (como boleto).
* **Edição de Cadastros:** Clientes podem editar seus dados cadastrais, mas a exclusão definitiva só é feita pela gerência.
* **Descontos:** Limite fixado entre 5% e 10% baseado no valor total da compra.
* **Políticas de Estoque:** Conferência física mensal e reposição conforme as vendas efetuadas.
* **Conformidade Legal:** Coleta e tratamento de dados adequados à LGPD.

---

## 10. Fluxogramas
![Fluxograma de Processos](img/fluxograma.png)

---

## 11. Dicionário de dados conceitual

| Entidade | Atributo | Descrição | Regra / Observação |
| :--- | :--- | :--- | :--- |
| **Pessoa** | `CPF` | Identificador único da pessoa | **PK** - Obrigatório e único |
| **Pessoa** | `Nome` | Nome completo | Obrigatório |
| **Pessoa** | `Email` | Correio eletrônico | Formato de e-mail válido |
| **Pessoa** | `Telefone` | Telefone de contato | Obrigatório |
| **Pessoa** | `Data_Nascimento` | Data de nascimento | Formato Data |
| **Cliente** | `ID_Cliente` | Identificador do cliente | **PK** - Auto incremento |
| **Cliente** | `Endereço` | Endereço completo para entrega | Obrigatório |
| **Cliente** | `CPF` | CPF da pessoa associada | **FK** referenciando `Pessoa(CPF)` |
| **Funcionário** | `ID_Funcionário` | Identificador do funcionário | **PK** |
| **Funcionário** | `Cargo` | Função na empresa | Ex: Vendedor, Gerente |
| **Funcionário** | `Salario` | Remuneração mensal | Valor monetário positivo |
| **Funcionário** | `Setor` | Setor de atuação | Ex: Vendas, Logística |
| **Funcionário** | `CPF` | CPF da pessoa associada | **FK** referenciando `Pessoa(CPF)` |
| **Fornecedor** | `Código_Fornecedor` | Identificador do fornecedor | **PK** |
| **Fornecedor** | `Matéria-Prima` | Descrição do insumo | Texto |
| **Fornecedor** | `Custo_Unitario` | Custo de aquisição do item | Valor monetário |
| **Fornecedor** | `CPF` | Documento do responsável/empresa | **FK** referenciando `Pessoa(CPF)` |
| **Compra** | `ID_Compra` | Registro da ordem de compra | **PK** |
| **Compra** | `Código_Fornecedor` | Código do fornecedor | **FK** referenciando `Fornecedor` |
| **Compra** | `Total_Gasto` | Valor gasto na compra | Valor monetário |
| **Produto** | `Código_Produto` | Código identificador do produto | **PK** |
| **Produto** | `Descrição` | Especificação técnica e nome | Texto |
| **Produto** | `Valor_Unitario` | Preço de venda ao consumidor | Valor monetário |
| **Estoque** | `Código_Produto` | Código do produto em estoque | **PK / FK** referenciando `Produto` |
| **Estoque** | `Informação` | Detalhes do lote e armazenamento | Texto |
| **Estoque** | `Quantidade_De_Cada_Produto` | Unidades/m² em estoque | Numérico inteiro/decimal |
| **Estoque** | `Abastecimento` | Frequência de reposição | Semanal ou Mensal |
| **Pedido** | `Código_Pedido` | Identificador único do pedido | **PK** |
| **Pedido** | `Data_De_Entrega` | Data prevista de instalação/entrega | Formato Data |
| **Pedido** | `Pagamento_Total` | Valor final do pedido | Valor monetário |
| **Pedido** | `Acréscimos` | Custos extras (frete/mão de obra) | Valor monetário |
| **Realiza** | `ID_Cliente` | Código do cliente | **FK** referenciando `Cliente` |
| **Realiza** | `Código_Pedido` | Código do pedido | **FK** referenciando `Pedido` |
| **Realiza** | `Subtotal` | Valor acumulado do cliente no pedido | Atributo próprio do relacionamento |
| **Contém** | `Código_Pedido` | Código do pedido | **FK** referenciando `Pedido` |
| **Contém** | `Código_Produto` | Código do produto | **FK** referenciando `Produto` |
| **Contém** | `Quantidade_De_Produtos` | Quantidade comprada do produto | Numérico |

---

## 12. Entidades
`Pessoa` – `Cliente` – `Funcionário` – `Fornecedor` – `Compra` – `Produto` – `Estoque` – `Pedido` – `Realiza` – `Contém`

---

## 13. Atributos
* **Pessoa:** `CPF (PK)` – `Nome` – `Email` – `Telefone` – `Data_Nascimento`
* **Cliente:** `ID_Cliente (PK)` – `Endereço` – `CPF (FK)`
* **Funcionário:** `ID_Funcionário (PK)` – `Cargo` – `Salario` – `Setor` – `CPF (FK)`
* **Fornecedor:** `Código_Fornecedor (PK)` – `Matéria-Prima` – `Custo_Unitario` – `CPF (FK)`
* **Compra:** `ID_Compra (PK)` – `Código_Fornecedor (FK)` – `Total_Gasto`
* **Produto:** `Código_Produto (PK)` – `Descrição` – `Valor_Unitario`
* **Estoque:** `Código_Produto (PK/FK)` – `Informação` – `Quantidade_De_Cada_Produto` – `Abastecimento`
* **Pedido:** `Código_Pedido (PK)` – `Data_De_Entrega` – `Pagamento_Total` – `Acréscimos`
* **Realiza:** `ID_Cliente (FK)` – `Código_Pedido (FK)` – `Subtotal`
* **Contém:** `Código_Pedido (FK)` – `Código_Produto (FK)` – `Quantidade_De_Produtos`

---

## 14. Relacionamentos

* **Pessoa – Cliente / Funcionário / Fornecedor:** Relacionamento de Especialização/Herança.
* **Cliente – Pedido (via "Realiza"):** O cliente realiza um ou mais pedidos.
* **Pedido – Produto (via "Contém"):** O pedido contém um ou múltiplos produtos registrados.
* **Fornecedor – Compra:** O fornecedor fornece produtos para as ordens de compra.
* **Compra – Produto:** As compras alimentam o catálogo e entrada de produtos.
* **Produto – Estoque:** Associação 1:1 entre o produto e suas informações de saldo de estoque.

---

## 15. Cardinalidades

* **Pessoa -> Cliente / Funcionário / Fornecedor:** `(0,1)` para `(1,1)`. Uma pessoa pode ser cadastrada como cliente, funcionário ou fornecedor.
* **Cliente -> Pedido ("Realiza"):** `(0,N)` para `(1,1)`. Um cliente pode realizar zero ou vários pedidos, mas um pedido pertence a um único cliente.
* **Pedido -> Produto ("Contém"):** `(1,N)` para `(0,N)`. Um pedido contém pelo menos 1 produto e um produto pode estar contido em vários pedidos (Relacionamento N:M).
* **Fornecedor -> Compra:** `(0,N)` para `(1,1)`. Um fornecedor pode estar em várias compras, e cada compra está associada a 1 fornecedor.
* **Produto -> Estoque:** `(1,1)` para `(1,1)`. Cada produto cadastrado possui exatamente 1 registro de controle de estoque correspondente.

---

## 16. Diagrama Entidade-Relacionamento (DER)
![Diagrama Entidade Relacionamento](img/der.png)

---

## 17. Justificativas técnicas das principais decisões de modelagem

1. **Adoção da Especialização/Herança com a Entidade `Pessoa`:**  
   Permite centralizar os dados cadastrais básicos de pessoas físicas (`CPF`, `Nome`, `Email`, `Telefone`) evitando campos duplicados entre clientes, funcionários e fornecedores.
2. **Uso das Entidades Associativas `Contém` e `Realiza`:**  
   O relacionamento N:M entre `Pedido` e `Produto` gerou a entidade `Contém` para armazenar a `Quantidade_De_Produtos` de cada item. Da mesma forma, `Realiza` armazena o `Subtotal` gerado pelo cliente.
3. **Separação entre `Produto` e `Estoque`:**  
   A Personal Pisos realiza controle mensal/semanal e vendas sob encomenda. Isolar o `Estoque` em uma estrutura 1:1 permite gerenciar lotes e quantidades sem alterar o cadastro fixo do `Produto`.
4. **Definição de Chave Primária em `Produto`:**  
   Corrigiu-se a identificação do `Código_Produto` para Chave Primária (`PK`), garantindo a integridade referencial nas tabelas associativas.

---

## 18. Conclusão
Esta entrega estabelece o Modelo Conceitual formal para a Personal Pisos, estruturando os requisitos coletados em entidades, atributos, relacionamentos e regras de negócio. O modelo atende às necessidades operacionais e de gestão da empresa e serve como base sólida para a próxima fase do projeto (Modelo Lógico, Normalização e DDL em Banco de Dados Relacional).
