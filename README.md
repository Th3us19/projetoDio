# projetoDio
Desafio do Guerreiro, mago, ninja, etc..

class Heroi {
  constructor(nome, idade, tipo) {
    this.nome = nome;
    this.idade = idade;
    this.tipo = tipo.toLowerCase(); // garantir letras minúsculas para comparar
  }

  atacar() {
    let ataque;

    switch (this.tipo) {
      case "mago":
        ataque = "usou magia";
        break;
      case "guerreiro":
        ataque = "usou espada";
        break;
      case "monge":
        ataque = "usou artes marciais";
        break;
      case "ninja":
        ataque = "usou shuriken";
        break;
      default:
        ataque = "fez um ataque desconhecido";
    }

    console.log(`O ${this.tipo} atacou usando ${ataque}`);
  }
}

// Testando a classe com diferentes heróis
const heroi1 = new Heroi("Arthus", 30, "guerreiro");
const heroi2 = new Heroi("Merlin", 70, "mago");
const heroi3 = new Heroi("Lee", 40, "monge");
const heroi4 = new Heroi("Hanzo", 25, "ninja");

heroi1.atacar(); // O guerreiro atacou usando usou espada
heroi2.atacar(); // O mago atacou usando usou magia
heroi3.atacar(); // O monge atacou usando usou artes marciais
heroi4.atacar(); // O ninja atacou usando usou shuriken
