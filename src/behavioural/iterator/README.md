# Iterator - Behavioural (Comportamental)

*Fornece uma maneira de acessar sequencialmente os elementos de um objeto agregado sem expor sua representação subjacente.*

---

## Sobre o Iterator

O Iterator é um padrão de design comportamental que fornece uma maneira de acessar os elementos de uma coleção de objetos de maneira sequencial, sem expor a representação interna da coleção. Com o padrão Iterator, é possível percorrer a coleção sem conhecer o tipo de dados subjacente, tornando o código mais flexível e extensível.

O padrão Iterator é implementado com um objeto Iterator, que fornece métodos para acessar os elementos da coleção. O objeto Iterator mantém um ponteiro para o próximo elemento da coleção e, ao ser chamado, retorna o próximo elemento. Quando todos os elementos da coleção foram percorridos, o Iterator retorna uma indicação para indicar que não há mais elementos disponíveis.

Por exemplo, imagine que você tem uma lista de tarefas e deseja percorrer cada tarefa. Usando o padrão Iterator, você pode criar um objeto Iterator para a lista de tarefas, que permitirá percorrer cada tarefa sem precisar acessar diretamente a lista. Isso torna o código mais fácil de ler e de entender, e permite que você adicione ou remova tarefas da lista sem afetar o código que percorre a lista.

---

## Usabilidade

Use o Iterator quando:

- Você precisa remover a complexidade de travessia de dentro da coleção principal. Isso permite que sua coleção foque apenas em armazenar dados de maneira eficiente
- Sua coleção pode ter vários modos de travessia, como crescente, decrescente,  pelo menor número de saltos, pulando de dois em dois, ou como preferir
- Você quer disponibilizar protocolos de travessia para diferentes tipos coleções

---

**Vantagens:**
- É possível pausar a travessia e continuar posteriormente
- É possível atravessar várias vezes a mesma coleção em paralelo usando outro objeto iterador
- É fácil adicionar novos objetos iteradores com algoritmos de travessia completamente diferentes
- Não polui o código do objeto principal com vários métodos e algoritmos de travessia diferentes

**Desvantagens:**
- Este padrão só é útil se sua coleção realmente precisar de uma travessia complexa. Do contrário é apenas complexidade a mais.
