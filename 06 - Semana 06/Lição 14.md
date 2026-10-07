# Lição 14: COLLISION DETECTION

**Avaliação:** A avaliação pede que use um nova ferramenta dentro da condicional if para identificar quando duas sprites se tocam, depois de se tocarem deve mudar a animação da sripte do cavalo para um unicornio. O desafio necessita que use um propriedade que mostra a área de interação de uma sprite com .debug = true, isso mostra o exato momento que as sprite vão se tocar.

```JavaScript
// create the sprites
var horse = createSprite(200, 150);
horse.setAnimation("horse");
horse.debug = true;
var rainbow = createSprite(400, 370);
rainbow.setAnimation("rainbow");
rainbow.velocityX = -5;
rainbow.velocityY = -5;
rainbow.rotateToDirection = true;
rainbow.debug = true;

function draw() {
  // draw the background
  background("skyblue");
  if (horse.isTouching(rainbow)){
    horse.setAnimation("unicorn");
  }

  // change the horse to a unicorn when the rainbow touches it
  
  drawSprites();
}
```

**Desafio:**  Nesse desafio, tive que criar um jogo completo, com controles e interações específicas para cada objetivo. O sapo tem sua animação de salto criada junto com uma condicional que controla a altura do pulo e o pouso. Essa parte foi a mais difícil para mim.
Depois, tive que criar duas sprites com movimento, que caminham em direção ao sapo. Quando atingem o limite do mapa ou são tocadas, precisam voltar ao seu lugar de origem.
Cada toque do sapo na mosca adiciona um ponto, enquanto cada toque no cogumelo faz o jogador perder uma vida. Quando o número de vidas chega a 0, o jogo acaba e imprime na tela a mensagem "Game Over".

```JavaScript
//GAME SETUP
// Create the sprites
var fundo = createSprite(200,200);
fundo.setAnimation("fundo");
var cogumelo = createSprite(450,370);
cogumelo.setAnimation("mushroom");
cogumelo.scale = 1;
cogumelo.velocityX = -3;
cogumelo.debug = true;
var sapo = createSprite(70,370);
sapo.setAnimation("frog");
sapo.scale = 1;
sapo.debug = true;
var mosca = createSprite(460,200);
mosca.setAnimation("fly");
mosca.scale = 1;
mosca.velocityX = -5;
mosca.debug = true;
// set velocity for the obstacle and the target


//create the variables
var score = 0;
var health = 100;

function draw() {
  // BACKGROUND
  background("lightblue");
  // draw the ground and other background

  // SPRITE INTERACTIONS
  if (sapo.isTouching(cogumelo)){
  health = health - 10;
  cogumelo.x = 450;
  }
  // if the player touches the obstacle
  // the health goes down, and the obstacle turns
  if(sapo.isTouching(mosca)){
    score = score +1;
    mosca.x = 460;
  }
  // if the frog touches the fly
  // the score goes up, the fly resets

  // JUMPING
  if (keyDown("up")){
    sapo.velocityY = -6;
  }
  if (sapo.y < 190){
    sapo.velocityY = 6;
  }
  // if the player has reached the ground
  if (sapo.y > 371){
    sapo.velocityY =0;
    sapo.y = 370;
  }
  // stop moving down

  // if the player presses the up arrow
  // start moving up

  // if the player reaches the top of the jump
  // start moving down

  // LOOPING
  if (cogumelo.x < -10){
    cogumelo.x = 450;
  }
  if (mosca.x < -10){
    mosca.x = 460;
  }
  // if the obstacle has gone off the left hand side of the screen, 
  // move it to the right hand side of the screen

  // if the target has gone off the left hand side of the screen,
  // move it to the right hand side of the screen

  // DRAW SPRITES
  drawSprites();
  
  // SCOREBOARD
  // add scoreboard and health meter
  fill("black");
  textSize(20);
  text("Health:", 280, 30);
  text (health, 350, 30);
  // GAME OVER
  // if health runs out
  // show Game over
  if (health < 1) {
    background("black");
    fill("green");
    textSize(50);
    text("Game Over!" , 40, 200);
  }
}
```