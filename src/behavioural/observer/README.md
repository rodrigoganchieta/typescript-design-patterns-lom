# Observer - Behavioural (Comportamental)

*Define uma dependência um para muitos entre objetos, de modo que, quando um objeto muda de estado, todos os seus dependentes são automaticamente notificados e atualizados.*

---

## Sobre o Observer

O Observer é um padrão de design comportamental que permite que objetos sejam notificados automaticamente quando ocorrem alterações em um objeto observado. Em outras palavras, esse padrão permite que um ou mais objetos sejam informados quando uma mudança de estado ocorrer em um objeto subjacente, sem que eles precisem poluir o objeto subjacente com código de notificação.

O padrão Observer é implementado com dois tipos de objetos: o objeto observado (também conhecido como sujeito ou publicador) e o objeto observador (também conhecido como assinante ou ouvinte). O objeto observado mantém uma lista de objetos observadores interessados em receber notificações e, quando ocorre uma mudança de estado no objeto observado, ele notifica todos os objetos observadores registrados na lista.

Por exemplo, imagine que você está desenvolvendo um aplicativo de previsão do tempo e deseja notificar os usuários quando as condições do tempo mudarem. Usando o padrão Observer, você pode criar um objeto WeatherData que é observado por vários objetos WeatherDisplay. Quando as condições do tempo mudam, o objeto WeatherData notifica todos os objetos WeatherDisplay registrados, que atualizam suas informações para refletir as novas condições.

---

## Usabilidade

Use o Observer quando:

- Você precisa notificar vários objetos sobre a mudança de estado de outro(s) objeto(s)

---

**Vantagens:**
- Usa o SRP e OCP
- Facilita a comunicação entre objetos em tempo de execução

**Desvantagens:**
- Pode ser complexo ou impossível manter a ordem em que as notificações são enviadas
