# Chain Of Responsibility - Behavioural (Comportamental)

*Evitar o acoplamento do remetente de uma solicitação ao seu destinatário, dando a mais de um objeto a chance de tratar a solicitação. Encadeia os objetos receptores e passa a solicitação ao longo da cadeia até que um objeto a trate*

---

## Sobre o Chain Of Responsibility

grupo de objetos lide com solicitações em uma ordem específica. Neste padrão, cada objeto recebe a solicitação e decide se a processa ou a passa para o próximo objeto na cadeia. Isso permite que vários objetos possam processar a solicitação, cada um com sua própria lógica de negócios, sem que o cliente precise saber qual objeto específico está lidando com a solicitação.

Por exemplo, imagine que uma empresa recebe pedidos de clientes através de vários canais, como telefone, e-mail e site. Cada canal pode ter sua própria equipe de atendimento ao cliente responsável por processar os pedidos recebidos. Usando o padrão Chain of Responsibility, cada equipe pode ser representada por um objeto na cadeia. Quando um pedido é recebido, ele é passado para o primeiro objeto na cadeia. Esse objeto decide se pode lidar com a solicitação ou passá-la para o próximo objeto na cadeia, e assim por diante, até que um objeto possa lidar com o pedido.

O Chain of Responsibility ajuda a simplificar o código e reduzir a complexidade, pois cada objeto pode se concentrar apenas na lógica de negócios que é responsável. Além disso, permite que a lógica de negócios seja facilmente alterada ou adicionada, sem afetar o restante do código.

---

## Usabilidade

Use o Chain Of Responsibility quando:

- seu sistema precisa processar uma requisição em várias etapas diferentes e você não quer criar uma ordem rígida para o processamento. O chain of responsibility permite que você altere a ordem dos objetos na cadeia facilmente (mesmo assim, mantendo uma ordem específica)
- você quer aplicar o princípio da responsabilidade única para tratamento de dados da requisição. Cada objeto fica responsável por tratar apenas a parte que lhe couber
- você quer permitir que os objetos responsáveis pelo tratamento de requisição possam variar em tempo de execução

---

**Vantagens:**
- Aplica o princípio da responsabilidade única (SRP)
- Aplica o princípio do aberto e fechado (OCP)
- Permite que você altere a cadeia de objetos e a ordem das chamadas facilmente

**Desvantagens:**
- É comum uma requisição passar por toda a cadeia e não ser tratada
