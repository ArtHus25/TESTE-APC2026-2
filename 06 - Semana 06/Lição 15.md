# Lição 15: COMPLEX SPRITE MOVEMENT

**Avaliação:** Utilizando váriações no movimento nessa avaliação para tornar os movimentos mais plásticos, tive que mudar a velocidade da pedra de maneira variada para dar um impressão de gravidade, usei como inspiração vídeos das missões espaciais com os objetos flutuando perdendo velocidade e caindo devagar.

```JavaScript

var rock = createSprite(200, 350);
rock.setAnimation("rock");
rock.velocityY =  - 25;
rock.rotationSpeed = 2;

function draw() {
  background("skyblue");
  rock.velocityY = rock.velocityY + 1;
  if (rock.y > 370){
    rock.velocityY = - 25;
  }
  


  
  // update sprites
  
  drawSprites();
}
```

**Desafio:** Seguindo na ideia de manipular os movimento para deixar as animações mais realistas devemos mudar a movimentação do avião para passar de maneira correta desviando das pedras. Usei um aumento progressivo de velocidade para dar impressão de parada e depois um freio junto com a mudança de direção quando chega no topo para desviar da pedra.

```JavaScript
var plane = createSprite(50, 350);
plane.setAnimation("plane");
var rock = createSprite(150, 350);
rock.setAnimation("rock");
var rockdown = createSprite(350, 100);
rockdown.setAnimation("rock_down");

// You might want to change these 
plane.velocityY = -8;
plane.velocityX = 3;

function draw() {
  background("lightblue");
  plane.velocityX = plane.velocityX + 0.1;
  if (plane.x > 160){
    plane.velocityY = plane.velocityY + 0.8;
  }
  
  // Make the Y velocity more downward
  
  drawSprites();
}
```