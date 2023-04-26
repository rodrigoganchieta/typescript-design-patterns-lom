# Prototype - Creational (Criação)

*Especificar os tipos de objetos a serem criados usando uma instância-protótipo e criar novos objetos pela cópia desse protótipo.*

---

## Sobre o Prototype

A intenção acima significa que você pode criar objetos protótipos que têm um método específico (`clone`) para clonar seus dados em um novo objeto. Isso evita a recriação de objetos caros ou complexos para serem criados.

---

## Usabilidade

Use o Prototype quando:

- Precisar que seu código não dependa de classes concretas para a criação de novos objetos
- Evita explosão de subclasses para objetos muito similares
- Evita a recriação de objetos "caros" ou "complexos"

---

**Vantagens:**
- Oculta classes concretas do código cliente
- Ajuda na criação de objetos caros ou complexos
- Evita a explosão de subclasses

**Desvantagens:**

- Clonar objetos que que tem referências para outros objetos pode ser super complexo
