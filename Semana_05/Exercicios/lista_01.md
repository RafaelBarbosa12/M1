# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

**a) Imprime os números pares de 1 a 10.**

b) Imprime os números ímpares de 1 a 10.

**c) Imprime os números pares de 2 a 10.**

d) Imprime os números ímpares de 2 a 10.

O número começa em 1 e é somado de um a um até chegar em 10 (determinado pelo while), a condição pega todos os números que possuem resto da divisão por 2 igual a 0, ou seja, todos os pares começando do 1 e indo até o 10.

Essa questão tem duas alternativas corretas já que vão ser impressos os números pares de 1 a 10 (já que o um não é par, ele não será impresso, mas continua sendo os números pares de 1 a 10) e os números de 2 a 10, mas dessa vez, o 2 já está incluído.


______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

**A) let carro = new Carro("Toyota");**

B) let ligar = new ligar("Toyota");

C) class Moto extends Veiculo {};

D) carro1.ligar();

Falta criar uma variavel que instancie a classe Carro

______

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

**A) 18**

B) 16

C) 14

D) 12

O I começa em 10 e diminui de 2 em 2, resultado += 10 é igual a 10, resultado+= 8 é igual a 18, agora o i vai passar pelo 6 e dar break, ou seja, o codigo será finalizado.
______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?

**A) ![Uma imagem](assets/ex04_1.PNG)**

B) ![Uma imagem](assets/ex04_2.PNG)

C) ![Uma imagem](assets/ex04_3.PNG)

D) ![Uma imagem](assets/ex04_4.PNG)

você precisa ter um construtor que inicializa o velocidadeAtual, apenas uma das alternativas faz isso.

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

**A) ![Uma imagem](assets/ex05_1.PNG)**

B) ![Uma imagem](assets/ex05_2.PNG)

C) ![Uma imagem](assets/ex05_3.PNG)

D) ![Uma imagem](assets/ex05_4.PNG)

você precisa ter um constructor para a marca e um metódo para o ligar
______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

**A) "Olá, meu nome é João. Olá, meu nome é Maria."**

B) "Olá, meu nome é ."

C) "João Maria"

D) "undefined undefined"

O console.log chama duas vezes a função greet, uma para cada nome, tendo a saída: "Olá, meu nome é João. Olá, meu nome é Maria."

______

# Questões dissertativas

**7)** Vamos criar um programa em JavaScript para entender classes, métodos e atributos!
Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método chamado descrever() na classe Animal.
  - Este método deve exibir no console uma descrição do animal com seu nome e idade.

Criando e manipulando Animais:
- Crie dois objetos da classe Animal: um chamado "cachorro" e outro "gato", com idades distintas.
- Para cada animal, chame o método descrever() para ver a descrição no console.

Dica: Utilize `console.log()` para exibir as informações!

```
class Animal{
    constructor(nome, idade){
        this.nome = nome;
        this.idade = idade;
    }

descrever(){
    console.log("Meu nome é " + this.nome + " e tenho ", this.idade + " anos");
}
}
var cachorro = new Animal("Leo pelé", 5)
var gato = new Animal("Veggeti", 6)

cachorro.descrever()
gato.descrever()
```
______

**8)** Nos últimos dias tivemos a oportunidade de ter contato com Programação Orientada a Objetos, e tivemos contato com o tema "herança". Herança é um princípio de orientação a objetos, que permite que classes compartilhem atributos e métodos. Ela é usada na intenção de reaproveitar código ou comportamento generalizado ou especializar operações ou atributos. Então vamos praticar esse conteúdo nessa questão.
Vamos criar um programa em JavaScript para entender classes, métodos, atributos e herança!

Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método descrever() que exiba no console uma descrição do animal com seu nome e idade.

Classe Gato (Herda de Animal):
- Crie uma classe chamada Gato que herda da classe Animal.
- Adicione um atributo extra cor específico para gatos.
- Adicione um método miar() que exiba no console o som que um gato faz.

Criando Animais:
- Crie dois objetos da classe Animal: um chamado cachorro e outro gato, com idades distintas.
- Para o gato, também defina a cor.

Chamando os Métodos:
- Para cada animal, chame o método descrever() para ver a descrição no console.
- Para o gato, chame o método miar() para "ouvir" o som que ele faz (é também para ver o som no console).

Dica: Utilize console.log() para exibir as informações!

```
class Animal{
    constructor(nome, idade){
        this.nome = nome;
        this.idade = idade;
    }

descrever(){
    console.log("Meu nome é " + this.nome + " e tenho ", this.idade + " anos");
}
}

class Gato extends Animal{
    constructor(nome, idade, cor){
        super(nome, idade);
        this.cor = cor
    }
    miar(){
        console.log("miauu")
    }
    descrever(){
        console.log("Meu nome é " + this.nome + ", tenho ", this.idade + " anos e minha cor é ", this.cor);
    }
}
var gato = new Animal("Pantera", 15)
var cachorro = new Animal("Hulk", 12);
var gatinho = new Gato("Neve", 2, "branco")
gato.descrever()
gatinho.descrever()
gatinho.miar()
cachorro.descrever()
```


______

**9)** Vamos criar um programa em JavaScript para somar notas!

Classe SomadorDeNotas:
- Crie uma classe chamada SomadorDeNotas.
- Adicione um atributo total inicializado com 0 para armazenar a soma das notas.

Método adicionarNota:
- Adicione um método chamado adicionarNota(nota) na classe SomadorDeNotas.
- Este método deve receber um parâmetro nota e somá-lo ao atributo total.

Criando o Somador e Adicionando Notas:
- Crie um objeto da classe SomadorDeNotas, chamado somador.
- Utilize o método adicionarNota(nota) para adicionar algumas notas ao somador.

Chamando o Método para Ver o Total:
- Após adicionar todas as notas, chame um método verTotal() para exibir o total das notas adicionadas.

Dica: Utilize console.log() para exibir as informações!

```
//cria a classe somador
class SomadorDeNotas{
    constructor(){
        this.total = 0
    }

    somarNota(nota){
        this.total += nota
        return this.total;
    }
    verTotal(){
        console.log(this.total)
    }

}
var somador = new SomadorDeNotas()
somador.somarNota(10)
somador.somarNota(9)
somador.somarNota(8)
somador.verTotal()
```


______

**10)** Imagine que você está criando um programa em JavaScript para uma escola. Neste programa, existem diferentes tipos de funcionários, cada um com suas próprias características. Considere as seguintes classes:

Funcionário:
- atributo: Nome
- atributo: Idade
- atributo: Salário base
- método: calcularSalario() - Este método calcula o salário total do funcionário. Para cada tipo de funcionário, o cálculo será diferente.

Professor (herança de Funcionário):
- atributo: Disciplina
- atributo: Horas de aula por semana
- método: calcularSalario() - Para calcular o salário do professor, multiplicamos suas horas de aula pelo valor da hora/aula.

Agora, sua tarefa é escrever um código em JavaScript que crie as classes Funcionário e Professor, com suas características e métodos descritos acima. Depois de criar as classes, crie:
- Dois objetos do tipo Professor com informações fictícias.
- Para cada objeto, chame o método calcularSalario() e mostre o salário calculado no console.

Certifique-se de explicar cada parte do código utilizando comentários, explicando para que serve cada atributo e método, bem como a lógica por trás do cálculo de salário para o tipo de funcionário Professor.

```
//classe Funcionario é criada

class Funcionario{

    //Inicialização do constructor para iniciar os valores das propriedades que serão usadas

    constructor(nome, idade, salarioBase){
        this.nome = nome;
        this.idade = idade;
        this.salarioBase = salarioBase;
    }
    calcularSalario(){
    }
}

//A classe Professor herda todas as caracteristicas de Funcionario

class Professor extends Funcionario{

    //inicia os valores

    constructor(nome, idade, salarioBase, disciplina, horasSemanais){

    //herda as referências da classe principal

        super(nome, idade, salarioBase);

    //referencáa as novas variáveis

        this.disciplina = disciplina;
        this.horasSemanais = horasSemanais;
    }
    //função para calcular salário

    calcularSalario(){

        //O salário é dado pela multiplicação de seu salario base pelas horas semanais

        //o salário base é dado por hora
        return(this.salarioBase * this.horasSemanais)
    }
}
//cria as novas instâncias de Professor

var professor1 = new Professor("Carlos", 35, 15, "matematica", 24)
var professor2 = new Professor("Luisa", 32, 17, "fisíca", 20)
var professor3 = new Professor("Giovana", 24, 16, "UX", 28)
var professor4 = new Professor("Lucas", 54, 19, "ingês", 16)

//printa quanto cada professor ganha por semana

console.log(professor1.nome, " ganha ", professor1.calcularSalario() + " reais por semana")
console.log(professor2.nome, " ganha ", professor2.calcularSalario() + " reais por semana")
console.log(professor3.nome, " ganha ", professor3.calcularSalario() + " reais por semana")
console.log(professor4.nome, " ganha ", professor4.calcularSalario() + " reais por semana")
```