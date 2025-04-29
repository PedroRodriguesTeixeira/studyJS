# studyJS

Para saber se algo é igual, você deve utilizar '==='.

Node.js consegue executar código JavaScript fora de um navegador web porque ele é construído sobre um componente específico, originalmente desenvolvido pelo Google para o Chrome. Esse componente é chamado de Interpretador JavaScript v8.

Ser uma linguagem multiparadigma significa que JavaScript não força o desenvolvedor a seguir um único paradigma de programação. É possível escrever código de forma procedural, utilizando funções e estruturas de controle; orientada a objetos, com classes e herança (prototipal em JavaScript); ou funcional, utilizando funções como cidadãs de primeira classe e evitando efeitos colaterais.

 Sendo JavaScript uma linguagem "interpretada com tipagem dinâmica fraca", qual das seguintes afirmações MELHOR descreve as consequências práticas disso para o desenvolvedor?
 O tipo de uma variável só é conhecido durante a execução, pode mudar durante o ciclo de vida da variável, e o JavaScript tenta automaticamente converter tipos (coerção) em operações, o que pode levar a resultados inesperados se não for bem compreendido.

Tipagem Dinâmica Fraca:
Nuança: JavaScript decide o tipo da variável em tempo de execução e tenta implicitamente converter tipos em muitas operações. Isso pode levar a resultados inesperados se não for bem compreendido.
Anotação Estratégica: Dinâmica (tipo runtime), Fraca (converte tipos implicitamente). Exemplo mental: '5' + 3 resulta em '53', mas '5' - 3 resulta em 2.

var tem escopo de função ou global (se declarada fora de qualquer função), sofrendo hoisting (a declaração é movida para o topo do escopo, mas a inicialização não).
let e const têm escopo de bloco e não sofrem hoisting da mesma forma (há uma "temporal dead zone"). const também exige inicialização e não pode ser reatribuída (a ligação, não necessariamente o valor interno se for um objeto).
Anotação Estratégica: var (função/global, hoisting), let/const (bloco, sem hoisting "forte"). const: não reatribui (ligação).

Coerção de Tipos (== vs ===). == tenta converter, === compara valor.
