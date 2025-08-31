# Oficina-Mecanica: Desafio-Dio
🛠️ Descrição do Desafio
Este projeto tem como objetivo desenvolver um esquema conceitual para um sistema de controle e gerenciamento de ordens de serviço (OS) em uma oficina mecânica. 

A proposta parte de uma narrativa que descreve o funcionamento básico da oficina, seus processos e os principais elementos envolvidos.
O esquema conceitual foi criado do zero, com base na narrativa fornecida. 
Quando necessário, foram feitas inferências e complementações para garantir a consistência e completude do modelo. 
Essas decisões estão documentadas abaixo para facilitar a avaliação.

📚 Contexto do Sistema
A oficina mecânica realiza serviços de manutenção e revisão em veículos trazidos por clientes. O processo de atendimento envolve diversas etapas:
- O cliente leva o veículo à oficina.
- O veículo é atribuído a uma equipe de mecânicos.
- A equipe identifica os serviços necessários e preenche uma Ordem de Serviço (OS).
- A OS inclui a data de emissão, data prevista para conclusão, status, valor estimado e os serviços a serem realizados.
- Os serviços são precificados com base em uma tabela de referência de mão de obra.
- Peças utilizadas também são incluídas na OS e impactam o valor final.
- O cliente autoriza a execução dos serviços.
- A mesma equipe realiza os serviços descritos na OS.

🧩 Entidades e Relacionamentos
Com base na narrativa, foram identificadas as seguintes entidades principais:
- Cliente: Representa a pessoa que leva o veículo à oficina. Possui atributos como ID, nome, endereço, CPF e telefone.
- Veículo: Cada veículo está associado a um cliente. Os atributos incluem placa, modelo, marca, Km, ano de fabricação e uma referência ao cliente proprietário.
- Mecânico: Profissional responsável pela execução dos serviços. Possui código identificador, nome e especialidade. 
- Equipe: Agrupamento de mecânicos que atua em conjunto na avaliação e execução dos serviços. Cada equipe possui um identificador, nome e categoria da equipe. 
- Ordem de Serviço (OS): Documento que formaliza os serviços a serem realizados. Contém número, data de emissão, data prevista para conclusão, valor total e status. 
Está relacionada a um veículo e a uma equipe responsável.
- Serviço: Representa uma atividade a ser realizada no veículo, como troca de óleo ou alinhamento. Cada serviço possui um identificador, descrição e valor de referência de mão de obra.
- Peça: Itens utilizados na execução dos serviços. Cada peça possui um código, nome e valor unitário.
- OS_Serviço: Relacionamento entre uma OS e os serviços que ela inclui. Permite registrar a quantidade de vezes que um serviço foi realizado e o valor total correspondente.
- OS_Peça: Relacionamento entre uma OS e as peças utilizadas. Permite registrar a quantidade de cada peça e o valor total correspondente

🔍 Observações e Inferências
- Cliente: A narrativa não especifica atributos, então foram incluídos os básicos para identificação e contato.
- Equipe: Criada como entidade para representar o agrupamento de mecânicos. A relação entre equipe e mecânicos é de 1-N.
- Serviço e Peça: Modelados separadamente para permitir reutilização e precificação individual.
- OS_Serviço e Peça_OS: Tabelas associativas para representar os itens incluídos em cada OS.
- Status da OS: Pode ser modelado como enumeração (Ex: "Pendente", "Autorizada", "Em Execução", "Concluída").

📁 Repositório
Este esquema conceitual está disponível neste repositório para avaliação. O modelo pode ser representado graficamente em formato de diagrama ER (Entidade-Relacionamento)
Link: 
