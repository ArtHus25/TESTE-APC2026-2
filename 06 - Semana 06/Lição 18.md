# Lição 18: Design a Game

**Projeto Final:** Criei um Jogo em que o jogador controla um personagem que precisa atravessar diferentes pistas com carros e caminhões em movimento. O objetivo é chegar ao final do mapa sem ser atingido pelos veículos. Caso o personagem seja atingido, perde um ponto e retorna ao início da fase. Quando consegue chegar ao final, ganha um ponto e também retorna ao início, podendo continuar jogando e acumulando pontos.
Além dos veículos, adicionei árvores como obstáculos para aumentar um pouco a dificuldade do jogo. Quando o personagem encosta em uma árvore, ele sofre um pequeno knockback, sendo empurrado para trás.
Para criar os elementos visuais do jogo, utilizei desenhos de uma biblioteca pública de imagens 2D, incluindo o personagem, carros, caminhões e árvores.
A maior dificuldade durante o desenvolvimento foi organizar as diversas functions utilizadas no código e fazer com que os elementos do cenário fossem reposicionados de maneira aleatória. Dessa forma, os carros, caminhões e árvores não aparecem sempre nas mesmas posições, deixando cada tentativa um pouco diferente e tornando o jogo mais dinâmico.

```JavaScript
// Create your variables here
var Score = 0;

// Create your sprites here
//Jogador
var Jogador = createSprite(200,380);
Jogador.setAnimation("Jogador1frente");
Jogador.scale = 3;
Jogador.debug = true;

// carros 
var carro1 = createSprite();
carro1.setAnimation("Carro1");
carro1.scale = 2;
setcarro1();
carro1.velocityX = 2;
carro1.debug = true;

var carro2 = createSprite();
carro2.setAnimation("carro2");
carro2.scale = 2;
setcarro2();
carro2.velocityX = 2;
carro2.debug = true;

var carro3 = createSprite();
carro3.setAnimation("Carro3");
carro3.scale = 2;
setcarro3();
carro3.velocityX = 2;
carro3.debug = true;

// caminhao
var caminhao = createSprite();
caminhao.setAnimation("Caminhão");
caminhao.scale = 3;
setcaminhao();
caminhao.velocityX = -2;
caminhao.debug = true;

var caminhao2 = createSprite();
caminhao2.setAnimation("Caminhão2");
caminhao2.scale = 3;
setcaminhao2();
caminhao2.velocityX = -2;
caminhao2.debug = true;

//Arvores
var arvore1 = createSprite();
arvore1.setAnimation("Arvore1");
arvore1.scale = 2;
setarvore1();
arvore1.velocityX = -2;
arvore1.debug = true;
var arvore2 = createSprite();
arvore2.setAnimation("Arvore2");
arvore2.scale = 2;
setarvore2();
arvore2.velocityX = -2;
arvore2.debug = true;
var arvore3 = createSprite();
arvore3.setAnimation("Arvore3");
arvore3.scale = 2;
setarvore3();
arvore3.velocityX = +2;
arvore3.debug = true;
var arvore4 = createSprite();
arvore4.setAnimation("Arvore4");
arvore4.scale = 2;
setarvore4();
arvore4.velocityX = +2;
arvore4.debug = true;

function draw() {
  // draw background
  gameBackground();
  moverjogador();
  encostarnocarro();
  encostarnaarvore();
  carrosair();
  caminhaosair();
  chegarfim();
  showscore();
  arvoresair();

  // update sprites

  drawSprites();
}

// Create your functions here
  // Fundo verde
function gameBackground() {
  noStroke();

  // Fundo verde
  background(color(50, 180, 70));

  // Pista 1
  fill(color(80, 80, 80));
  rect(0, 0, 400, 70);

  // Pista 2
  rect(0, 155, 400, 80);

  // Pista 3
  rect(0, 310, 400, 70);

  // Linhas das pistas
  fill(color(255, 255, 255));

  // Pista 1
  rect(0, 0, 400, 5);
  rect(0, 70, 400, 5);

  // Pista 2
  rect(0, 155, 400, 5);
  rect(0, 230, 400, 5);

  // Pista 3
  rect(0, 310, 400, 5);
  rect(0, 375, 400, 5);
}

// Mover jogador
function moverjogador(){
  if (keyDown("up")){
    Jogador.y = Jogador.y - 3;
    Jogador.setAnimation("Jogador1costas");
  }
  
  if (keyDown("down")){
    Jogador.y = Jogador.y + 3;
    Jogador.setAnimation("Jogador1frente");
  }
  
  if (keyDown("left")){
    Jogador.x = Jogador.x - 3;
    Jogador.setAnimation("Jogador1esquerda");
  }
  
  if (keyDown("right")){
    Jogador.x = Jogador.x + 3;
    Jogador.setAnimation("Jogador1direita");
  }
}
// Encostar nos carros
function encostarnocarro(){
  if (Jogador.isTouching(carro1)){
    Score = Score - 1;
    Jogador.x = 200;
    Jogador.y = 380;
  }
    if (Jogador.isTouching(carro2)){
    Score = Score - 1;
    Jogador.x = 200;
    Jogador.y = 380;
  }
    if (Jogador.isTouching(carro3)){
    Score = Score - 1;
    Jogador.x = 200;
    Jogador.y = 380;
  }
    if (Jogador.isTouching(caminhao)){
    Score = Score - 1;
    Jogador.x = 200;
    Jogador.y = 380;
  }
    if (Jogador.isTouching(caminhao2)){
    Score = Score - 1;
    Jogador.x = 200;
    Jogador.y = 380;
  }
}

function encostarnaarvore(){
  if (Jogador.isTouching(arvore1)){
    Jogador.y = Jogador.y + 5;
  }
   if (Jogador.isTouching(arvore2)){
    Jogador.y = Jogador.y + 5;
  }
   if (Jogador.isTouching(arvore3)){
    Jogador.y = Jogador.y + 5;
  }
   if (Jogador.isTouching(arvore4)){
    Jogador.y = Jogador.y + 5;
  }
}

function carrosair(){
  if (carro1.x > 400){
    setcarro1();
    
  }
  if (carro2.x > 400){
    setcarro2();
    
  }
  if (carro3.x > 400){
    setcarro3();
    
  }
}
function caminhaosair(){
  if (caminhao.x < - 20){
    setcaminhao();
  }
  if (caminhao2.x < - 20){
    setcaminhao2();
  }
}
function arvoresair(){
  if (arvore1.x < -5){
    setarvore1();
  }
  if (arvore2.x < -5){
    setarvore2();
  }
  if (arvore3.x > 410){
    setarvore3();
  }
  if (arvore4.x > 410){
    setarvore4();
  }
  
}
function chegarfim(){
  if(Jogador.y <  -5){
    Score = Score + 1;
    Jogador.x = 200;
    Jogador.y = 380;
  }
}

function showscore (){
    fill("white");
  textSize(20);
  text("Score",20,20,200,100);
  text(Score,20,40,200,100);
}

function setcarro1(){
  carro1.x = randomNumber(-50,-5);
  carro1.y = 200;
}
function setcarro2(){
  carro2.x = randomNumber(-92,-7);
  carro2.y = 330;
}
function setcarro3(){
  carro3.x = randomNumber(-125,-9);
  carro3.y = 30;
}
function setcaminhao(){
  caminhao.x = randomNumber(420,460);
  caminhao.y = 330;
  
}
function setcaminhao2(){
  caminhao2.x = randomNumber(430,560);
  caminhao2.y = 30;
  
}
function setarvore1(){
  arvore1.x = randomNumber(400,690);
  arvore1.y = 270;
  
}
function setarvore2(){
  arvore2.x = randomNumber(410,670);
  arvore2.y = 270;
}
function setarvore3(){
  arvore3.x = randomNumber(-90,-5);
  arvore3.y = 110;
}
function setarvore4(){
  arvore4.x = randomNumber(-120,-15);
  arvore4.y = 110;
}
```