# Lição 12: MOUSE INPUT

**Avaliação:** Essa avaliação foi bem desafiadora, usando agora o mouse com interação nas imagens usamos condicionais quando o mouse for apertado a sprite deve tremer e o texto parar de aparecer, a primerira parte é fácil mas fazer o texto desaparecer somente em quanto o mouse está sendo apertado que foi difícil. Tive que colocar um condicional de IF e Else a mais quando o mouse está sendo apertado nada acontecer e quando não estiver ai sim pode imprimir o texto em tela.

```JavaScript
var backdrop = createSprite(200,200);
backdrop.setAnimation("sky");
var creature = createSprite(200,250);
creature.setAnimation("creature");
creature.scale = 0.2;
function draw() {
  //shake the sprite when the mouse is pressed
  if(mouseDown()){
  creature.rotation = randomNumber(-5,5);
  }
   drawSprites();
  //display the text when the mouse is NOT pressed
  if(mouseDown()){
    
  }
  else{
  fill("black");
  textSize(40);
  text("Press the mouse to shake the creature.", 20, 50, 360, 100);
}
    
  }
```

**Desafio:**  O desafio pedia duas coisas tornar a sprite móvel apartir do movimento do mouse, usando a nova condicional Worl.MouseX e Y a imagem tem sua posição mudada apartir do movimento do mouse. Depois o desafio pediu para adiconar mais sprites seguindo o mouse e que a posição mude com números aleatórios para passar a impressão de movimento real de uma abelha.

```JavaScript
World.frameRate = 20;
var abelha = createSprite(200,200);
abelha.setAnimation("bee");
abelha.scale = 0.5;
var abelha2 = createSprite(200,200);
abelha2.setAnimation("bee2");
abelha2.scale = 0.5;
var abelha3 = createSprite(200,200);
abelha3.setAnimation("bee3");
abelha3.scale = 0.5;

function draw(){
  background("lightblue");
  if(World.mouseX){
    abelha.x = World.mouseX+ randomNumber(-50,50);
    abelha2.x = World.mouseX + randomNumber(-40,40);
    abelha3.x = World.mouseX + randomNumber(-30,40);
  }
  if(World.mouseY){
    abelha.y = World.mouseY+randomNumber(-50,50);
    abelha2.y = World.mouseY+randomNumber(-40,40);
    abelha3.y = World.mouseY+randomNumber(-30,30);
  }
  drawSprites();
}
``` 