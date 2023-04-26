# Visitor - Behavioural (Comportamental)

*Representa uma operação a ser executada sobre os elementos da estrutura de um objeto. O visitor permite que você separe um algoritmo dos elementos sobre os quais opera.*

---

## Sobre o Visitor
O Visitor é um padrão de design comportamental que permite que novas operações sejam adicionadas a uma hierarquia de classes existente sem alterar as classes existentes. Em outras palavras, esse padrão permite adicionar novas funcionalidades a uma classe sem precisar alterar a própria classe.

O padrão Visitor é implementado com duas partes principais: o objeto visitante e a hierarquia de classes visitáveis. O objeto visitante é uma classe que define novas operações que podem ser aplicadas à hierarquia de classes visitáveis. A hierarquia de classes visitáveis é composta por uma série de classes que aceitam visitantes e implementam um método "accept" que permite que os visitantes acessem seus atributos e métodos.

Por exemplo, imagine que você está desenvolvendo um sistema de processamento de arquivos que precisa de diferentes tipos de processamento de acordo com o tipo de arquivo. Usando o padrão Visitor, você pode criar uma hierarquia de classes visitáveis, como ImageFile, TextFile e AudioFile, e um objeto visitante, como FileProcessor, que implementa diferentes operações de processamento para cada tipo de arquivo. Quando um objeto FileProcessor é aplicado a um objeto visitável, como uma ImageFile, ele chama o método "accept" do ImageFile, que permite que o FileProcessor acesse os atributos e métodos do ImageFile e execute a operação apropriada.

---

## Usabilidade

Use o Visitor quando:

- você precisa executar um algoritmo em todos os elementos de uma estrutura mais complexa (como uma estrutura criada com o padrão Composite)
- Você quer separar uma lógica complexa em objetos auxiliares

---

**Vantagens:**
- Limpa o código da regra de negócio
- Separa algoritmos complexos em objetos auxiliares
- Aplica SRP e OCP

**Desvantagens:**
- Se um novo objeto for adicionado à estrutura, você precisará atualizar os objetos visitantes
- Objetos visitantes podem não ter acesso a todos os membros dos objetos em que operam
