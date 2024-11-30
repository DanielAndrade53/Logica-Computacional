# Trabalho Prático 3

Nota: 

Problema 1

O [algoritmo estendido de Euclides](https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm) (EXA) aceita dois inteiros constantes a,b>0 e 
devolve inteiros r,s,t tais que a*s + b*t = r e r = gcd(a,b). 

Para além das variáveis r,s,t o código requer 3 variáveis adicionaiscr',s',t' que
representam os valores de r,s,t no “próximo estado”.
    
    INPUT  a, b
    assume  a > 0 and b > 0
    r, r', s, s', t, t' = a, b, 1, 0, 0, 1
    while r' != 0
      q = r div r'
      r, r', s, s', t, t' = r', r − q × r', s', s − q × s', t', t − q × t' 
    OUTPUT r, s, t
    


1. Construa um SFOTS usando BitVector’s de tamanho n que descreva o
comportamento deste programa.  Considere estado de erro quando r=0 ou
alguma das variáveis atinge o “overflow”.
3. Prove, usando a metodologia dos invariantes e interpolantes, que o modelo nunca
atinge o estado de erro.

Problema 2

Relativo ao programa do problema anterior,

1. Construa um “Control Flow Automaton (CFA)” que determina este programa.
2. Identifique os locais e as transições/ramos.  Numa abordagem orientada às
pré-condições  identifique os transformadores de predicados associados aos vários
 locais e os “switches” associados aos vários ramos. 
4. Construa em z3 o sistema de equações que representa o comportamento deste
sistema dinâmico sob o ponto de vista da prova de segurança e verifique a
segurança do programa através da resolução (total ou parcial) deste sistema.
> sugere-se (não é obrigatório mas é valorizado !), na alínea (a), uma representação do
CFA através de  um grafo orientado  implementado  em networkx  e a sua compilação
para o sistema de equações.
    
Problema 3

Considere de novo o 1º problema do trabalho TP2  relativo à descrição da cifra A5/1 e o
FOTS usando BitVec’s que aí foi definido para a componente do gerador de chaves. Ignore
a componente de geração final da chave e restrinja o modelo aos três LFSR’s. 
Sejam X0, X1, X2 as variáveis que determinam os estados dos três LFSR’s que ocorrem
neste modelo. Como condição inicial e condição de erro use os predicados

I = (X0 > 0) ∧ (X}1 > 0) ∧ (X2 > 0) e E = ¬I 

1. Codifique em “z3”  o SFOTS assim definido.
2. Use o algoritmo PDR “property directed reachability” (codifique-o ou use uma
versão pré-existente) e, com ele, tente provar a segurança deste modelo.
