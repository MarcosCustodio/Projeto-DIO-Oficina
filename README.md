Sistema de Controle e Gerenciamento de Ordens de Serviço - Oficina Mecânica
Este projeto é um sistema de controle e gerenciamento de ordens de serviço para uma oficina mecânica. O objetivo é automatizar e otimizar os processos de atendimento aos clientes, controle de ordens de serviço, e execução de reparos e revisões em veículos. O sistema gerencia o relacionamento entre clientes, veículos, mecânicos, serviços realizados e peças utilizadas, além de calcular o valor total de cada ordem de serviço com base no tempo de trabalho e peças usadas.

Funcionalidades Principais
Cadastro de Clientes e Veículos: Permite registrar clientes e seus respectivos veículos, mantendo um histórico de manutenção para cada veículo.
Gestão de Ordens de Serviço: Criação e gerenciamento de ordens de serviço, incluindo a definição de serviços a serem executados, peças a serem utilizadas e o cálculo do valor total da ordem de serviço.
Atribuição de Mecânicos: Permite designar equipes de mecânicos para a execução das ordens de serviço, levando em consideração suas especialidades e disponibilidade.
Tabela de Mão de Obra: O sistema consulta uma tabela de referência para calcular o valor da mão de obra de cada serviço, com base no tempo estimado para a execução das tarefas.
Controle de Peças: Gestão de peças utilizadas nas ordens de serviço, com a possibilidade de reutilização de peças em diferentes ordens.
Autorização do Cliente: O cliente autoriza a execução dos serviços através da ordem de serviço, podendo visualizar o valor estimado antes da execução.
Status da Ordem de Serviço: O status da ordem de serviço pode ser alterado, indicando se está em andamento, concluída, ou cancelada.

Entidades e Relacionamentos
O esquema de banco de dados foi desenvolvido com base nas seguintes entidades principais:

Cliente: Contém informações sobre os clientes, como nome, endereço, telefone e e-mail.
Veículo: Relacionado a um cliente, cada veículo possui um histórico de ordens de serviço.
Mecânico: Registra informações sobre os mecânicos, incluindo nome, endereço e especialidade.
Ordem de Serviço: Cada ordem de serviço está associada a um veículo e cliente, contendo o número da ordem, data de emissão, status, valor total e data de conclusão.
Serviço: Refere-se aos serviços realizados (ex: troca de óleo, revisão de freios) e é associado a uma ordem de serviço.
Peça: Refere-se às peças utilizadas nas ordens de serviço, com informações sobre o preço e descrição.
Tabela de Mão de Obra: Define o valor da mão de obra para diferentes tipos de serviço, permitindo calcular o valor total da ordem de serviço.
Relaciones principais entre as entidades:
Cliente -> Veículo: Um cliente pode ter vários veículos, mas cada veículo pertence a um único cliente.
Veículo -> Ordem de Serviço: Cada veículo pode ter várias ordens de serviço associadas.
Ordem de Serviço -> Mecânico: Cada ordem de serviço pode ser atribuída a vários mecânicos, e cada mecânico pode trabalhar em várias ordens de serviço.
Ordem de Serviço -> Serviço: Uma ordem de serviço pode conter vários serviços, e um serviço pode ser realizado em várias ordens de serviço.
Ordem de Serviço -> Peça: Uma ordem de serviço pode utilizar várias peças, e uma peça pode ser utilizada em diversas ordens de serviço.
Serviço -> Tabela de Mão de Obra: O valor de cada serviço é calculado com base na tabela de mão de obra.
