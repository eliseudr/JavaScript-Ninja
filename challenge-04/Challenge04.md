# Desafio da semana #4

```js
/*
Declare uma variável chamada `isTruthy`, e atribua a ela uma função que recebe
um único parâmetro como argumento. Essa função deve retornar `true` se o
equivalente booleano para o valor passado no argumento for `true`, ou `false`
para o contrário.
*/
var isTruthy = function (arg){
    return !!arg;
    }
}

// Invoque a função criada acima, passando todos os tipos de valores `falsy`.
isTruthy(0);
isTruthy(-0);
isTruthy(null);
isTruthy();
isTruthy('');
isTruthy(undefined);

/*
Invoque a função criada acima passando como parâmetro 10 valores `truthy`.
*/
var isTruthy = function(arg1, arg2, arg3, arg4, arg5, arg6, arg7, arg8, arg9, arg10){
... return !!arg1, !!arg2, !!arg3, !!arg4, !!arg5, !!arg6, !!arg7, !!arg8, !!arg9, !!arg10;
... }

isTruthy(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
//true

/*
Declare uma variável chamada `carro`, atribuindo à ela um objeto com as
seguintes propriedades (os valores devem ser do tipo mostrado abaixo):
- `marca` - String
- `modelo` - String
- `placa` - String
- `ano` - Number
- `cor` - String
- `quantasPortas` - Number
- `assentos` - Number - cinco por padrão
- `quantidadePessoas` - Number - zero por padrão
*/
var carro = {
    marca: "Volks",
    modelo: "Gol",
    placa: "CDI 1111",
    ano: 2004,
    cor: "Prata",
    quantasPortas: 4,
    assentos: 5,
    quantidadePessoas: 0
};

/*
Crie um método chamado `mudarCor` que mude a cor do carro conforme a cor
passado por parâmetro.
*/
carro.mudarCor = function (novaCor){
    carro.cor =  novaCor;
}

/*
Crie um método chamado `obterCor`, que retorne a cor do carro.
*/
carro.obterCor = function (){
    return carro.cor;
}

/*
Crie um método chamado `obterModelo` que retorne o modelo do carro.
*/
carro.obterModelo = function (){
    return carro.modelo;
}

/*
Crie um método chamado `obterMarca` que retorne a marca do carro.
*/
carro.obterMarca = function (){
    return carro.marca;
}

/*
Crie um método chamado `obterMarcaModelo`, que retorne:
"Esse carro é um [MARCA] [MODELO]"
Para retornar os valores de marca e modelo, utilize os métodos criados.
*/
carro.obterMarcaModelo = function (){
    return "Esse carro é um " + carro.marca + " " + carro.modelo;
}

/*
Crie um método que irá adicionar pessoas no carro. Esse método terá as
seguintes características:
- Ele deverá receber por parâmetro o número de pessoas entrarão no carro. Esse
número não precisa encher o carro, você poderá acrescentar as pessoas aos
poucos.
- O método deve retornar a frase: "Já temos [X] pessoas no carro!"
- Se o carro já estiver cheio, com todos os assentos já preenchidos, o método
deve retornar a frase: "O carro já está lotado!"
- Se ainda houverem lugares no carro, mas a quantidade de pessoas passadas por
parâmetro for ultrapassar o limite de assentos do carro, então você deve
mostrar quantos assentos ainda podem ser ocupados, com a frase:
"Só cabem mais [QUANTIDADE_DE_PESSOAS_QUE_CABEM] pessoas!"
- Se couber somente mais uma pessoa, mostrar a palavra "pessoa" no retorno
citado acima, no lugar de "pessoas".
*/
carro.adicionarPessoa = function (NumDePessoas){
    carro.quantidadePessoas += NumDePessoas;

    if(carro.quantidadePessoas >= 5){
        return "O carro já está lotado!";
    } else if( carro.quantidadePessoas < 4){
        return "Só cabem mais " + (5 - carro.quantidadePessoas) + " pessoas!";
    } else {
        return "Só cabe mais uma pessoa !!";
    }

    return "Já temos " + carro.quantidadePessoas + " pessoas no carro!";
}

/*
Agora vamos verificar algumas informações do carro. Para as respostas abaixo,
utilize sempre o formato de invocação do método (ou chamada da propriedade),
adicionando comentários _inline_ ao lado com o valor retornado, se o método
retornar algum valor.

Qual a cor atual do carro?
*/
// prata

// Mude a cor do carro para vermelho.
//undefined

// E agora, qual a cor do carro?
//Vermelho

// Mude a cor do carro para verde musgo.
//undefined

// E agora, qual a cor do carro?
//Verde musgo

// Qual a marca e modelo do carro?
// 'Esse carro é um Volks Gol'

// Adicione 2 pessoas no carro.
//faltam 2 pessoas.

// Adicione mais 4 pessoas no carro.
//O carro ja esta lotado

// Faça o carro encher.
//O carro ja esta lotado

// Tire 4 pessoas do carro.
//So cabem mais 3 pessoas

// Adicione 10 pessoas no carro.
//O carro ja esta lotado

// Quantas pessoas temos no carro?
//12 pessoas
```
