public class Main {
    public static void main(String[] args) {
        // Criando um herói do tipo mago
        Heroi mago = new Heroi("Merlin", 150, "mago");
        mago.atacar();  // Chamando o método atacar do mago

        // Criando um herói do tipo guerreiro
        Heroi guerreiro = new Heroi("Arthur", 30, "guerreiro");
        guerreiro.atacar();  // Chamando o método atacar do guerreiro

        // Criando um herói do tipo monge
        Heroi monge = new Heroi("Li Shang", 40, "monge");
        monge.atacar();  // Chamando o método atacar do monge

        // Criando um herói do tipo ninja
        Heroi ninja = new Heroi("Hanzo", 25, "ninja");
        ninja.atacar();  // Chamando o método atacar do ninja
    }
}

// Classe que representa um herói
class Heroi {
    // Propriedades da classe
    String nome;
    int idade;
    String tipo;

    // Construtor da classe
    public Heroi(String nome, int idade, String tipo) {
        this.nome = nome;
        this.idade = idade;
        this.tipo = tipo;
    }

    // Método para realizar o ataque
    public void atacar() {
        String ataque = "";  // Inicializa a descrição do ataque

        // Verifica o tipo do herói e define a descrição do ataque
        switch (tipo) {
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
                ataque = "usou um ataque indefinido";
        }

        // Exibe a mensagem de ataque
        System.out.println("O " + tipo + " " + nome + " atacou usando " + ataque);
    }
}
