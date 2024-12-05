# Trabalho Pratico 2

Nota Problema 1: A
Nota Problema 2: A
Nota: A

Problema 1

Considere a descrição da cifra A5/1 que consta no documento [+Lógica Computacional: a
Cifra A5/1](https://paper.dropbox.com/doc/NwkyAeoKf0srn6MyQjWKP) . Informação complementar pode ser obtida no [artigo da Wikipedia](https://en.wikipedia.org/wiki/A5/1). 

Pretende-se
  1. Definir e codificar, em Z3 e usando o tipo BitVec para modelar a informação, uma
  FSM que descreva o gerador de chaves.
  3. Considere as seguintes eventuais propriedades de erro:
    1. ocorrência de um “burst” 0^t (t zeros) que ocorre em 2^t passos ou menos.
    2. ocorrência de um “burst” de tamanho t que repete um “burst” anterior
    no mesmo output em 2^{t/2}  passos ou menos.
  Tente codificar estas propriedades e verificar se são acessíveis a partir de um
  estado inicial aleatoriamente gerado.
    
Problema 2

Considere o problema descrito no documento [+Lógica Computacional: Multiplicação de 
Inteiros](https://paper.dropbox.com/doc/Logica-Computacional-Multiplicacao-de-Inteiros-n1G7pMihg2yJrMswfpBxr) . Nesse documento usa-se um “Control Flow Automaton” como  modelo 
do programa imperativo que calcula a multiplicação de  inteiros positivos representados por 
vetores de bits.

Pretende-se
  1. Construir um FOTS, usando BitVec’s de tamanho n , que descreva o
  comportamento deste autómato; para isso identifique e codifique em Z3  ou pySMT,
  as variáveis do modelo, o estado inicial , a relação de transição e o estado de erro.
  3. Usando k-indução verifique nesse SFOTS se a propriedade (x*y + z = a*b) é
  um invariante do seu comportamento.
  5. Usando k-indução no FOTS acima e adicionando ao estado inicial  a condição
  (a < 2^{n/2}) ∧ (b < 2^{n/2}), verifique a segurança do programa; nomeadamente
  prove que, com tal estado inicial, o estado de erro nunca é acessível.
