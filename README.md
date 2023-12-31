# Minecraft-Enchants-Front-End

A ideia desse projeto surgiu enquanto eu jogava Minecraft com meus amigos e parei para pensar sobre a tradução dos encantamentos do jogo, então cheguei na ideia de criar uma API para tal feito.
Este é o Front-End de exemplo para a requisição da API, caso queira ver com detalhes, aqui está a [API](https://github.com/Victor-Lis/Minecraft-Enchantments-Back-End)
# Desafios

### Como funciona?
Eu atribui um código de 2 digitos para cada caractere, logo é necessario basicamente passar uma sequência de códigos respectivos para cada caractere, retribuindo a tradução, segue um exemplo e a função.

### Exemplo
Nesse caso irei passar o seguinte código: 1924161924193035, respectivo ao encantamento "infinity" ou em português "infinidade".
```js
let data = await fetch(`http://localhost:4000/code-to-caracter?codes=1924161924193035`)
  .then(res => res.json())
      
if(data.data.length){
  console.log(data.data) // INFINITY
}
```

## Rota para traduzir Letras para os Caractéres do Minecraft

### Como funciona?
Simples, eu atribui as Letras como keys de um objeto e o respectivo caractere na frente, segue um exemplo e a função.

### Exemplo
Nesse caso irei escrever "infinity" o mesmo encantamento de cima.

```js
async function letterToEnchant() {
    let data = await fetch(`http://localhost:4000/letter-to-enchantment?text=INFINITY`)
        .then(res => res.json())
        .catch(e => console.log(e))

    console.log(data) // O resultado será o link das respectivas imagens dos caractéres
}
```

## Rota para receber um objeto das imagens e de seus códigos

### Como funciona?
Essa é a rota mais simples, sem lógica alguma, ela simplesmente retorna um objeto com as imagens como "Keys" do objeto e os códigos como "Values.

### Exemplo
```js
async function letterToEnchant() {
    let data = await fetch(`http://localhost:4000/images-codes`)
        .then(res => res.json())
        .catch(e => console.log(e))

    if (data) {
      console.log(data) // O resultado será o link das respectivas imagens dos caractéres
    }
}
```

## Projeto na prática

### Front-End
![Screen 1](https://raw.githubusercontent.com/Victor-Lis/Minecraft-Enchantments/main/src/images/Screenshot1.png)
![Screen 2](https://raw.githubusercontent.com/Victor-Lis/Minecraft-Enchantments/main/src/images/Screenshot2.png)

### Back-End
![Route 1](https://raw.githubusercontent.com/Victor-Lis/Minecraft-Enchantments/main/src/images/Back-End-Route1.png)
![Route 2](https://raw.githubusercontent.com/Victor-Lis/Minecraft-Enchantments/main/src/images/Back-End-Route2.png)
![Route 3](https://raw.githubusercontent.com/Victor-Lis/Minecraft-Enchantments/main/src/images/Back-End-Route3.png)


## Autores
- [@Victor-Lis](https://github.com/Victor-Lis)
