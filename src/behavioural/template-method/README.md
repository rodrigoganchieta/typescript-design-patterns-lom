# Template Method - Behavioural (Comportamental)

*Define o esqueleto de um algoritmo em uma operação, postergando a definição de alguns passos para subclasses. O template method permite que as subclasses redefinam certos passos de um algoritmo sem mudar sua estrutura*

---

## Sobre o Template Method
O Template Method é um padrão de design comportamental que permite que uma classe defina o esqueleto de um algoritmo em uma superclasse, mas permite que as subclasses substituam etapas específicas do algoritmo sem alterar sua estrutura global.

O padrão Template Method é implementado com uma classe abstrata que define o esqueleto do algoritmo e uma série de métodos abstratos que as subclasses devem implementar para personalizar o algoritmo. Os métodos abstratos são chamados em etapas específicas do algoritmo e permitem que as subclasses substituam o comportamento padrão.

Por exemplo, imagine que você está desenvolvendo um jogo de xadrez e deseja implementar a lógica de jogo. Usando o padrão Template Method, você pode criar uma classe abstrata ChessGame que define o esqueleto da lógica do jogo, incluindo a configuração do tabuleiro, o gerenciamento de turnos e a verificação de vitória. As subclasses de ChessGame, como ChessAIPlayer e ChessHumanPlayer, podem substituir as etapas específicas do algoritmo para personalizar o comportamento de acordo com suas necessidades.

---

## Usabilidade

Use o Template Method quando:

- Você precisa de variações de um mesmo algoritmo sem mudar a ordem de execução dos métodos
- Você percebe que está usando herança para alterar apenas pequenos trechos de código de um algoritmo

---

**Vantagens:**
- Evita duplicação de código
- Permite fácil alteração de algoritmos
- Aplica o OCP e SRP

**Desvantagens:**
- Em alguns casos pode violar o LSP ao alterar o comportamento de métodos nas subclasses
