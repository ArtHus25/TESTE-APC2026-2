# Lição 10: CONDITIONALS

**Avaliação:** Essa avaliação devemos usar uma condicional para checar quando o dinossouro atravessar o meio da tela, quando essa condição é atendida o variável muda de animação mudando a imagem do dinossauro para um pterodatilo.


```JavaScript
var backdrop = createSprite(200,200);
backdrop.setAnimation("sci_fi");
var dinosaur = createSprite(200, 350);
dinosaur.scale = 0.2;
dinosaur.setAnimation("tyrannosaurus");

function draw() {
  //move the dinosaur up
  dinosaur.y = dinosaur.y - 5;

  //if it gets to the sky, turn it into a pterodactyl
  if (dinosaur.y < 250){
    dinosaur.setAnimation("pterodactyl");
  }

  //draw everything
  drawSprites();
}
```

**Desafio:** O desafio foi  difícil, temos que dentro do drawn loop ir aumentando a escala do balão quando ele atingir os cantos da tela temos que tornar ele uma sprite invisível e carregar um variável escondida em visível para passar uma ilusão da troca de sprites.

```JavaScript
World.frameRate = 80;
var balloon = createSprite(200, 200);
balloon.setAnimation("balloon");
balloon.scale = 0.1;
balloon.visible = true;
var pop = createSprite(200,200);
pop.setAnimation("pop");
pop.scale = 1;
pop.visible = false;

function draw() {
  // Draw Background
  background("white");
  
  // Update Values
  balloon.scale = balloon.scale + 0.001;
  if (balloon.scale > 0.8){
    pop.visible=true;
    balloon.visible = false;
    
  }

  // Draw Animations
  drawSprites();
}
```