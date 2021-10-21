# compraevendadecarro
pragma solidity 0.8.9;

contract compraeVendaDeCarro {
    string comprador;
    string vendedor; 
    string documento;
    string dataDeVencimento;
    bool quitado = false;
    uint public valorTotal = 20000;
    uint public valorDaEntrada;
    uint public valorEmAberto;
    uint public quantidadeDeParcelas;
    uint public porcentagemDaMulta; 
    
    function pagarEntrada (uint _valorPagamento) public returns (uint, string memory) { 
        valorDaEntrada = _valorPagamento; 
        valorEmAberto = valorTotal - _valorPagamento;
        return(valorEmAberto, "valor em aberto");
    }  
