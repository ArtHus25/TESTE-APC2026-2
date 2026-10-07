# Lição 16: COLLISIONS

**Avaliação:** Essa avaliação foi bem divertida. Temos que usar todos os tipos de interações entra sprites, fazer uma sprite empurrar a outra, as duas se empurrarem em direções apostas, ou uma carregar a outra. Precisa de atenção para lembrar qual propriedade das interações usar na hora certa.

```JavaScript
// create sprites
var giraffe = createSprite(50, 50);
giraffe.setAnimation("giraffe");
giraffe.velocityX = 3;
var hippo = createSprite(50, 150);
hippo.setAnimation("hippo");
hippo.velocityX = 3;
var rabbit = createSprite(50, 250);
rabbit.setAnimation("rabbit");
rabbit.velocityX = 3;
var snake = createSprite(50, 350);
snake.setAnimation("snake");
snake.velocityX = 3;
var parrot = createSprite(350, 50);
parrot.setAnimation("parrot");
parrot.velocityX = -3;
var elephant = createSprite(350, 150);
elephant.setAnimation("elephant");
elephant.velocityX = -3;
var monkey = createSprite(350, 250);
monkey.setAnimation("monkey");
monkey.velocityX = -3;
var pig = createSprite(350, 350);
pig.setAnimation("pig");
pig.velocityX = -3;


function draw() {
  background("lightblue");
  giraffe.bounce(parrot);
  hippo.displace(elephant);
  monkey.displace(rabbit);
  snake.bounceOff(pig);
  drawSprites();
}
```

**Desafio:** Esse desafio foi muito interessante. Devemos investigar o porque das interações entre as sprite estarem se comportando de maneira errada. O formato da interação, usamos .debug para enxergar sua forma, é uma parte importantíssima para isso acontecer. No caso de programa as moedas estavam com formato de interação quadrado que não respeita o formato real de uma moeda e torna a interação entre as duas errada.

```JavaScript
//Código em JavaScript

var goldCoin = createSprite(49,50);
goldCoin.setAnimation("gold_coin");
goldCoin.velocityX = 2;
goldCoin.velocityY = 2;
goldCoin.debug = true;
goldCoin.setCollider("circle");

var silverCoin = createSprite(350,350);
silverCoin.setAnimation("silver_coin");
silverCoin.velocityX = -2;
silverCoin.velocityY = -2;
silverCoin.debug = true;
silverCoin.setCollider("circle");

function draw() {
  goldCoin.bounce(silverCoin);
  
  background("darkgreen");
  drawSprites();
}
```