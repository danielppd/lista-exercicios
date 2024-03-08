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

a) Imprime os números pares de 1 a 10.

b) Imprime os números ímpares de 1 a 10.

c) Imprime os números pares de 2 a 10. *-> resposta certa*

d) Imprime os números ímpares de 2 a 10.

______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

A) let carro = new Carro("Toyota"); *-> resposta certa*

B) let ligar = new ligar("Toyota");

C) class Moto extends Veiculo {};

D) carro1.ligar();

______

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

A) 18 *-> resposta certa*

B) 16

C) 14

D) 12

______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?

A) ![Uma imagem](assets/ex04_1.PNG) *-> resposta certa*

B) ![Uma imagem](assets/ex04_2.PNG)

C) ![Uma imagem](assets/ex04_3.PNG)

D) ![Uma imagem](assets/ex04_4.PNG)

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

A) ![Uma imagem](assets/ex05_1.PNG) *-> resposta certa*

B) ![Uma imagem](assets/ex05_2.PNG)

C) ![Uma imagem](assets/ex05_3.PNG)

D) ![Uma imagem](assets/ex05_4.PNG)

______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima? 

A) "Olá, meu nome é João. Olá, meu nome é Maria." *->resposta certa*

B) "Olá, meu nome é ."

C) "João Maria"

D) "undefined undefined"

______

# Questões dissertativas

**7)** 
class Animal {
    constructor(nome, idade){
        this.nome = nome; // adicionando o atributo nome à classe
        this.idade = idade; //adicionando o atributo idade à classe
    }
    descrever() {
        console.log(`Este é um ${this.nome} e ele possui ${this.idade} anos.`) //imprimindo o nome e idade do animal
    }
}

let animal1 = new Animal("cachorro", 9); // cria o objeto animal 1, que no caso é um cachorro com 9 anos de idade
let animal2 = new Animal("gato", 3); // cria o objeto animal 2, que no caso é um gato com 3 anos de idade

animal1.descrever() //utiliza o método presente na classe, fazendo imprimir o console log com as descrições do cachorro
animal2.descrever() //utiliza o método presente na classe, fazendo imprimir o console log com as descrições do gato
______

**8)** 
class Animal {
    constructor(nome, idade){
        this.nome = nome; // adicionando o atributo nome à classe
        this.idade = idade; //adicionando o atributo idade à classe
    }
    descrever() {
        console.log(`Este é um ${this.nome} e ele possui ${this.idade} anos.`) //imprimindo o nome e idade do animal
    }
}

class Gato extends Animal {
    constructor(nome,idade, cor) {
        super(nome, idade); //herda atributos da classe "pai"
        this.cor = cor //adiciona um novo atributo exclusivo da classe Gato
    }
    miar() {
        console.log(`O ${this.nome} ${this.cor} mia "miau! miau!"`) //imprime o miado informações do gato
    }
}

let animal1 = new Animal("cachorro", 12); //define o objeto animal1 
animal1.descrever(); //atribui a função descrever()
let gato1 = new Gato("gato", 7, "laranja") //define o objeto gato1 
gato1.descrever(); //atribui a função descrever()
gato1.miar(); //atribui a função miar()


______

**9)** 
class SomadorDeNotas{ *// cria a classe SomadorDeNotas*
    constructor() {
        this.total = 0 *// utilizado para armazenar a soma das notas*
    }
    adicionarNota(nota) {
        this.total += nota //soma cada nova nota ao valor total
    }
    verTotal() {
        console.log(`O total da soma das notas vale ${this.total}`) *// imprime o valor total da soma das notas*
    }
}

let somador = new SomadorDeNotas(); *// cria o objeto somador da classe SomadorDeNotas*
somador.adicionarNota(7); *// soma a nota 7 ao total*
somador.adicionarNota(9.2); *// soma a nota 9.2 ao total*
somador.adicionarNota(5.4); *// soma a nota 5.4 ao total*
somador.verTotal() *// chama a função para imprimir o valor total da soma das notas

*
______

**10)** 
class Funcionario{ *//cria  a passa "pai" Funcionario, que posteriormente servirá como base para a classe professor*
    constructor(nome, idade, salario_base){ 
        this.nome = nome 
        this.idade = idade
        this.salario_base = salario_base
    }
    calcularSalario(){
    }
}

class Professor extends Funcionario{
    constructor(nome, idade, salario_base, disciplina, horas_aula){
        super(nome, idade, salario_base) *//atributos herdados da classe "pai"*
        this.disciplina = disciplina *//adiciona o atributo disciplina (disciplina que o professor dá aula)*
        this.horas_aula = horas_aula *//adiciona o atributo horas_aula (quantidade de horas de aulas dadas semanalmente pelo professor)*
    }
    calcularSalario(){
        console.log(`O professor ${this.nome}, de ${this.idade} anos, da disciplina de ${this.disciplina}, que trabalha ${this.horas_aula} horas por semana e tem como salário base R$${this.salario_base}, recebe cerca de R$${this.salario_base * this.horas_aula * 4} de salário total`)
        *//função para imprimir o salário total do professor e outras informações pessoais dele*
        *//o salário dele é calculado a partir da multiplicação do salário base que ele possui, o quanto ele recebe por cada hora aula dada, multiplicado pelo total de horas de aulas dadas na semana, multiplicada por 4 (total de semanas presentes em um mês)*
    }
}

let professor1 = new Professor("Judson", 49, 200, "matemática", 40) *//define o objeto professor1 da classe Professor*
professor1.calcularSalario() *//chama a função calculaSalario que revela as informações e salário total do professor*
let professor2 = new Professor("Caio", 20, 70, "Física", 20)
professor2.calcularSalario()