# impostosVisualG

Algoritmo "semnome"

// Disciplina   : [Linguagem e Lógica de Programação]

Var
// Seção de Declarações das variáveis 
sbruto: real
sliquido: real
irrf: real
inss: real


Inicio

//Inicio

   Escreval ("Vamos calcular os impostos presentes em seu salário.")
   Escreval ("Qual seu salario bruto?")
   leia (sbruto)
   
//Calculo IRRF

   Se (sbruto < 2112.01) entao
   irrf <- 0
   senao
        se(sbruto < 2826.66) entao
        irrf <- 158.4
        senao
             se(sbruto < 3751.06) entao
             irrf <- 370.4
             senao
                  se (sbruto < 4664.69) entao
                  irrf <- 651.73
                  senao
                  irrf <- 884.96
                  fimse
             fimse
        fimse
   fimse
          
//Calculo INSS

   Se (sbruto < 1412.01) entao
   inss <- sbruto * 0.075
   senao
        Se (sbruto < 2666.69) entao
        inss <- sbruto * 0.09
        senao
             Se (sbruto < 4000.04) entao
             inss <- sbruto * 0.12
             senao
             inss <- sbruto * 0.14
             fimse
        fimse
   fimse

//Calculo Salario Liquido

sliquido <- sbruto - inss - irrf

//Final

Escreval ("Seu salário Liquído é de ", sliquido)
Escreval (" com os seguintes impostos:")
Escreval ("IRRF = ", irrf)
Escreval ("INSS = ", inss)

Fimalgoritmo
