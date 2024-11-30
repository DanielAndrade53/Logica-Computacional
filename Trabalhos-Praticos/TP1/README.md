# Trabalho Pratico 1

Problema 1

Pretende-se construir um horário semanal para o plano de reuniões de projeto de uma “StartUp” de acordo com as seguintes condições:

  1. Cada reunião ocupa uma sala (enumeradas 1...S) durante um “slot” (tempo,dia).  
  Assume-se os dias enumerados $$1..D$$ e, em cada dia, os tempos enumerados 1..T.
  2.  Cada reunião tem associado um projeto (enumerados 1..P) e um conjunto de 
  participantes. Os diferentes colaboradores são enumerados 1..C.
  3. Cada projeto tem associado um conjunto de colaboradores, dos quais um  é o líder. 
  Cada projeto realiza um dado número de reuniões semanais.
  São “inputs” do problema o conjunto de colaboradores de cada projeto, o seu líder
  e o número de reuniões semanais.
  5. O líder do projeto participa em todas as reuniões do seu projeto; os restantes
  colaboradores podem ou não participar consoante a sua disponibilidade, num
  mínimo (“quorum”) de  $$50\%$$ do total de colaboradores do projeto.  A disponibilidade
  de cada participante, incluindo o lider,  é um conjunto de “slots” (“inputs” do
  problema). 
    
Problema 2

Um sistema de tráfego é representado por um grafo orientado ligado. Os nodos denotam 
pontos de acesso e  os arcos denotam vias de comunicação só com um sentido .  O grafo 
tem de ser ligado: entre cada par de nodos <n_1,n_2> tem de existir um caminho n_1 -> n_2 e
um caminho n_2 -> n_1.

  1. Gerar aleatoriamente o grafo com  N in {6..10}  nodos e com ramos verificando:
    1. Cada nodo tem um número aleatório de descendentes d in {1 .. 3}, cujos destinos
    são também gerados aleatoriamente. 
    2. Se  existirem “loops” ou destinos repetidos, deve-se gerar outro grafo.
  3. Pretende-se fazer  manutenção interrompendo  determinadas vias. Determinar o
    maior número de vias que é possível remover mantendo o grafo ligado.
