# SA-LOPR
algoritmo "AlocacaoRecursos_Tigre"
var
   recurso, setor: caractere
   quantidadeTotal, quantidadeAlocada, quantidadeDisponivel, pedido: inteiro
inicio
   // Cadastro do recurso
   escreval("==== Sistema de Alocação de Recursos ====")
   escreva("Digite o nome do recurso: ")
   leia(recurso)
   escreva("Digite a quantidade total disponível do recurso: ")
   leia(quantidadeTotal)
   
   // Inicializando valores
   quantidadeAlocada <- 0
   quantidadeDisponivel <- quantidadeTotal
   
   enquanto verdadeiro faca
      escreval("==== Menu ====")
      escreval("1. Alocar recurso para um setor")
      escreval("2. Verificar disponibilidade")
      escreval("3. Sair")
      escreva("Escolha uma opção: ")
      leia(pedido)
      
      escolha pedido
      caso 1
         escreva("Digite o nome do setor: ")
         leia(setor)
         escreva("Digite a quantidade de recursos a alocar: ")
         leia(quantidadeAlocada)
         
         se quantidadeAlocada <= quantidadeDisponivel entao
            quantidadeDisponivel <- quantidadeDisponivel - quantidadeAlocada
            escreval("Recurso '", recurso, "' alocado com sucesso para o setor: ", setor)
            escreval("Quantidade restante: ", quantidadeDisponivel)
         senao
            escreval("Erro: Quantidade insuficiente de recursos disponíveis!")
         fimse
         
      caso 2
         escreval("Recurso: ", recurso)
         escreval("Quantidade Total: ", quantidadeTotal)
         escreval("Quantidade Disponível: ", quantidadeDisponivel)
         
      caso 3
         escreval("Saindo do sistema. Obrigado!")
         pare
         
      caso contrario
         escreval("Opção inválida. Tente novamente.")
      fimescolha
   fimenquanto
fimalgoritmo
