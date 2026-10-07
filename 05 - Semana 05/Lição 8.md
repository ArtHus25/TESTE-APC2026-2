# Lição 8 DRAWLOOP

**Avaliação:** Nessa Lição temos que usar o Drawn Loop para redesenhar a imagem e criar o movimento da cena, e fazer o saleiro se mover. O dificuldade desse desafio é saber quais comandos precisam ficar dentro do loop para que sejam constantemente atualizados na imagem. devemos colocar o backgound no loop para sobrepor a última imagem. No desafio tive que mudar a rotação da imagem para que o saleiro ficasse para baixo.

```JavaScript
var salt = createSprite(200,200);
salt.setAnimation("salt");
salt.rotation = 180;
function draw() {
  background("skyblue");
  salt.y = randomNumber(200,210);
 
drawSprites();

  
}
```


**Desafio:** Nessa desafio usamos um programa já construido no exercício anterior de texto para usar o drawnloop na animação das imagens. Eu usei o drawnloop para dar movimento aos personagens e a lava do cenário. foi um exercício bem legal que deu mais vida ao antigo projeto.

```JavaScript
World.frameRate = 10;
function draw() {
  // Background e lava
  var fundo = createSprite(200,100);
  fundo.setAnimation("fundo");
  var lava = createSprite(randomNumber(60,360),360);
  lava.setAnimation("lava");
  var lava1 = createSprite(randomNumber(60,360),362);
  lava1.setAnimation("lava");
  var lava2 = createSprite(randomNumber(60,360),362);
  lava2.setAnimation("lava");
  var lava3 = createSprite(randomNumber(60,360),362);
  lava3.setAnimation("lava");
  var lava4 = createSprite(randomNumber(60,360),362);
  lava4.setAnimation("lava");
  var lava5 = createSprite(randomNumber(60,360),362);
  lava5.setAnimation("lava");
  // Monstro e a Banana
  var monstro = createSprite();
  monstro.x = 100;
  monstro.y = randomNumber(180,200);
  monstro.setAnimation("monstro");
  monstro.scale = 0.3;
  var banana = createSprite();
  banana.x = 300;
  banana.y = 200;
  banana.setAnimation("banana");
  banana.scale = 0.3;
  banana.rotation = randomNumber(0,360);
  drawSprites();
  // Texto
  fill("red");
  stroke("black");
  strokeWeight(10);
  textSize(15);
  text("Its realy Hot",60,90);
  text("in here!!!",70,120);
  fill("yellow");
  stroke("green");
  strokeWeight(10);
  textSize(30);
  text("BANANA!!!",220,100);
}
```
