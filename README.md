# Contrato Inteligente Escrow

O contrato inteligente Escrow implementa um sistema de depósito, liberação e reembolso de fundos entre um comprador, vendedor e árbitro.

## Funcionalidades

### Constructor

- `constructor(address payable _buyer, address payable _seller, address payable _arbiter, uint _amount)`: Inicializa o contrato com os endereços do comprador, vendedor, árbitro e o valor a ser mantido em custódia.

### Funções Públicas

- `deposit() payable`: Permite que o comprador deposite os fundos no contrato, passando o valor a ser mantido em custódia. Somente o comprador pode executar essa função quando o contrato estiver no estado inicializado.

- `release()`: Permite que o árbitro libere os fundos para o vendedor. Somente o árbitro pode executar essa função quando o contrato estiver no estado bloqueado.

- `refund()`: Permite que o árbitro devolva os fundos ao comprador. Somente o árbitro pode executar essa função quando o contrato estiver no estado bloqueado.

### Enumerações

- `State`: Enumeração dos possíveis estados do contrato (Initialized, Locked, Released, Inactive).

## Uso

1. **Deploy do Contrato**: O contrato deve ser implantado na blockchain com os endereços do comprador, vendedor, árbitro e o valor do depósito.

2. **Depósito**: O comprador realiza um depósito usando a função `deposit`.

3. **Liberação**: O árbitro pode liberar os fundos para o vendedor usando a função `release`.

4. **Reembolso**: O árbitro pode reembolsar os fundos para o comprador usando a função `refund`.

## Referência Educacional

Este contrato foi desenvolvido com referências educacionais. Recomendamos o canal do YouTube [Nome do Canal](https://www.youtube.com/watch?v=w3wLT_u8dvE) como uma fonte adicional de aprendizado sobre contratos inteligentes.

## Autor

Canal Web3dev
Inspirado no vídeo: https://www.youtube.com/watch?v=w3wLT_u8dvE

## Licença

Este contrato é licenciado sob a Licença MIT. Consulte o arquivo [LICENSE.md](LICENSE.md) para detalhes.
