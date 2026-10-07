# Lição 11: KEYBOARD INPUT

**Avaliação:**  Esse desafio temos que fazer quatro condicionais para quando as setas do teclados sejam apertadas o movimento do anjo as sigam. Foi um desafio um pouco mais fácil sem muitas pegadinhas


```JavaScript
var backdrop = createSprite(200,200);
backdrop.setAnimation("rainbow");
var flyer = createSprite(200,200);
flyer.setAnimation("wing_bot");

function draw() {
    //move left when the left arrow is pressed
  if(keyDown("left")){
    flyer.x = flyer.x - 2;
  }
    //move right when the right arrow is pressed
  if(keyDown("right")){
    flyer.x = flyer.x + 2;
    }
   //move up when the up arrow is pressed
    if(keyDown("up")){
      flyer.y = flyer.y - 2;
    }
    //move down when the down arrow is pressed
    if(keyDown("down")){
      flyer.y = flyer.y + 2;
    }
  
  drawSprites();
}
```

**Desafio:** Esse desafio foi trabalhoso, dentro de cada condicional que vai determinar o movimento da mosca, devemos tambem criar uma animação nova para que o movimento da mosca acompanhe seu movimento, tive que criar três novas animação que assumem a imagem da variável mosca toda vez que a condicional das setas para mudar o movimento de X e Y da imagem junto com a forma correta da animação.

```JavaScript
var bug = createSprite(200, 200);
bug.setAnimation("fly");

function draw() {
  //Draw Background
  background("white");
  
  // Update Values
  if(keyDown("up")){
    bug.setAnimation("flyup");
    bug.y = bug.y - 5;

  }
  if(keyDown("down")){
    bug.setAnimation("flydown");
    bug.y = bug.y + 5;

  }
  if(keyDown("left")){
    bug.setAnimation("flyleft");
    bug.x = bug.x - 5;

  }
  if(keyDown("right")){
   bug.setAnimation("flyright");
    bug.x = bug.x + 5;

  }

  //Draw Animations
  drawSprites();
}
```