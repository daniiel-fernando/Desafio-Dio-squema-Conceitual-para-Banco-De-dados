# Sistema de Controle e Gerenciamento de Execução de Ordens de Serviço em Oficina Mecânica

Este projeto consiste na criação de um esquema conceitual para um sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica. O esquema proposto visa organizar e facilitar o gerenciamento das operações diárias de uma oficina, incluindo o registro de clientes, veículos, ordens de serviço, mecânicos, serviços prestados e itens associados.

## Esquema Conceitual

### Entidades Principais

1. **Cliente**
   - Atributos: idCliente (chave primária), Nome, Endereço

2. **Veículo**
   - Atributos: idVeiculo (chave primária), Marca, Modelo, Placa, Ano

3. **Ordem de Serviço (OS)**
   - Atributos: idOS (chave primária), Data de Emissão, Valor Total, Status, Data de Conclusão Prevista
   - Relacionamentos: Cliente (chave estrangeira: idCliente), Veículo (chave estrangeira: idVeiculo)

4. **Mecânico**
   - Atributos: idMecanico (chave primária), Código, Nome, Endereço, Especialidade

5. **Serviço**
   - Atributos: idServico (chave primária), Descrição, Valor

6. **Item de Serviço**
   - Atributos: idItemServico (chave primária), idOS (chave estrangeira), idServico (chave estrangeira), Quantidade

### Relacionamentos

- **Cliente <-> Veículo:** Um cliente pode possuir vários veículos.
- **Veículo <-> Ordem de Serviço:** Um veículo pode estar associado a várias ordens de serviço ao longo do tempo.
- **Mecânico <-> Ordem de Serviço:** Um mecânico pode ser atribuído a várias ordens de serviço.
- **Serviço <-> Item de Serviço:** Vários serviços podem ser realizados em uma mesma ordem de serviço.

### Descrição Adicional

- **Mão-de-obra:** Não especificada diretamente na narrativa, mas presume-se que seja um componente do serviço realizado pelos mecânicos, implicando em um cálculo de valor para cada serviço executado.

## Estrutura do Repositório

- **esquema_conceitual.sql:** Script SQL contendo as definições das tabelas e relacionamentos do esquema conceitual.
- **README.md:** Este arquivo, contendo a descrição do projeto, do esquema conceitual e outras informações relevantes.

## Contribuição

Sinta-se à vontade para sugerir melhorias ou modificações neste esquema conceitual através de pull requests. Todas as contribuições são bem-vindas!
