# Escrevendo-as-Classes-de-Um-Jogo
Ultimo-Desafio-Do-Felipao

 Desafio – Escrevendo as Classes de um Jogo

Projeto desenvolvido como parte dos desafios da **Digital Innovation One (DIO)**, com foco na prática de **Programação Orientada a Objetos em JavaScript**.

---

 Descrição do Desafio

Neste desafio, foi criado um sistema simples para representar **heróis de um jogo**, utilizando classes em JavaScript.

A classe deve conter:
- Nome do herói
- Idade
- Tipo do herói

Além disso, deve existir um método responsável por exibir uma mensagem de ataque, que varia de acordo com o tipo do herói.

---

 Tecnologias Utilizadas

- JavaScript (ES6)
- Programação Orientada a Objetos
- Plataforma DIO

---

 Conceitos Praticados

- Criação de classes
- Uso do método `constructor`
- Instanciação de objetos
- Estruturas condicionais (`switch`)
- Métodos de classe

---

 Tipos de Herói e Ataques

Conforme a lógica do desafio, cada tipo de herói realiza um ataque diferente:

| Tipo        | Ataque                       |
|-------------|------------------------------|
| banshee     | alteração de almas           |
| lobisomem   | garras sangrentas            |
| bruxa       | bola de energia amaldiçoada  |
| bersek      | avanço brutal                |

---

Implementação

```javascript
class Heroi {
  constructor(nome, idade, tipo) {
    this.nome = nome;
    this.idade = idade;
    this.tipo = tipo;
  }

  atacar() {
    let ataque;

    switch (this.tipo) {
      case "banshee":
        ataque = "alteração de almas";
        break;
      case "lobisomem":
        ataque = "garras sangrentas";
        break;
      case "bruxa":
        ataque = "bola de energia amaldiçoada";
        break;
      case "bersek":
        ataque = "avanço brutal";
        break;
      default:
        ataque = "ataque desconhecido";
    }

    console.log(`o ${this.tipo} atacou usando ${ataque}`);
  }
}

// Execução do desafio
const heroi = new Heroi("Nyx", 120, "banshee");
heroi.atacar();

