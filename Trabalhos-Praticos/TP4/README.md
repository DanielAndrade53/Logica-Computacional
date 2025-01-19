# Trabalho Prático 4

Nota Problema 1: A
Nota Problema 2: A
Nota: A

Problema 1

No contexto do sistema de travagem ABS (“Anti-Lock Breaking System”), pretende-se construir um autómato híbrido que descreva o sistema e que  possa ser usado para verificar as suas propriedades dinâmicas.
 
A componente discreta do autómato contém os modos: `Start`, `Free`, `Stopping`, `Blocked`, e `Stopped`. No modo `Free` não existe qualquer força de travagem; no modo `Stopping` aplica-se a força de travagem alta; no modo `Blocked` as rodas estão bloqueadas em relação ao corpo mas o veículo  desloca-se; no modo `Stopped` o veículo está imobilizado.

A componente contínua  do autómato usa variáveis contínuas  V ,v para descrever a  
`velocidade do corpo` do veículo em relação ao solo e a `velocidade linear das rodas` também em relação ao solo.  Assume-se que o sistema de travagem exerce uma força de atrito  nos travões proporcional à diferença das duas velocidades.  A dinâmica contínua está descrita  abaixo no bloco Equaçoes de Fluxo.

1. Defina um autómato híbrido que descreva a dinâmica do sistema segundo as notas abaixo indicadas e com os “switchs” por si escolhidos. Os “switchs” (“jumps”) são uma  componente de projeto deste trabalho; cabe ao aluno definir quais devem ser estas condições de modo a que o sistema tenha um comportamento desejável: imobilize-se depressa e não “derrape” muito.
2. Modele em lógica temporal linear LT  propriedades que caracterizam o comportamento desejável do sistema. Nomeadamente
   
   i. "o veículo imobiliza-se completamente em menos de t segundos"
   
   ii. "a velocidade V diminui sempre com o tempo".

3. Construa o FOTS que que descreve a discretização do  modelo  que definiu em 1. e codifique em SMT’s
4. Codifique a verificação das propriedades temporais que definiu em 2.

Problema 2

Este exercício é dirigido à <ins>à prova de correção</ins> do algoritmo de Euclides apresentado no trabalho TP3.

1. Construa a asserção lógica que representa a pós condição do algoritmo. Note que a definição da função gcd é gcd(a,b) ≡ min{r > 0 ∣ ∃s,t. r = a∗s+b∗t}.
2. Usando a metodologia do comando **havoc** para o ciclo, escreva o programa na linguagem dos comandos anotados (LPA). Codifique a pós condição do algoritmo com um commando **assert**.
3. Construa codificações do programa LPA através de transformadores de predicados "strongest post-condition" e prove a correção do programa LPA.
