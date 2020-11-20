## Trex Runner

1. #### P5 editor has 3 functions

   

   ```javascript
   function preload(){
    trex = loadAnimation("image1.png","image2.png")
   }
   //loading images, sounds and animations
   ```

   ```javascript
   function setup(){
     //creating sprites
       //adding images and animations
       trex = createSprite(50,160,20,50);
       trex.addAnimation("running", trex_running);
   }
   ```

   ```javascript
   function draw(){
   	background()
       
       //everything related to tha game
       // function draw runs many times, and frameCOunt gives the count of the run
       drawSprites();
   }
   ```

   2. #### creating the main hero of the game- trex

      ```javascript
      function preload(){
            trex_running = loadAnimation("trex1.png","trex3.png","trex4.png");
            trex_collided = loadAnimation("trex_collided.png");
        }
      
      function setup() {
            createCanvas(600, 200);
      
            trex = createSprite(50,160,20,50);
            trex.addAnimation("running", trex_running);
            // trex.addAnimation("collided",trex_collided)
            trex.scale = 0.5;
          //to resize the image size
        }
        
        function  draw(){
            background("grey")
            drawSprites
        }
      ```

      3. #### creating ground and invisible ground

         

         ground is the sand image  and invisible ground is the invisible sprite to make  the trex stand on.

         ```javascript
         var trex, trex_running, trex_collided;
         var ground, invisibleGround, groundImage;
         
         var cloud, cloudsGroup, cloudImage;
         
         
         
         var newImage;
         
         function preload(){
           trex_running = loadAnimation("trex1.png","trex3.png","trex4.png");
           trex_collided = loadAnimation("trex_collided.png");
           
           groundImage = loadImage("ground2.png");
          }
         
         function setup() {
           createCanvas(600, 200);
         
           trex = createSprite(50,160,20,50);
           trex.addAnimation("running", trex_running);
           // trex.addAnimation("collided",trex_collided)
           trex.scale = 0.5;
           
           ground = createSprite(200,180,400,20);
           ground.addImage("ground",groundImage);
           ground.x = ground.width /2;
           ground.velocityX = -4;
           // ground is moving towards left hence the velocity is -4
           
           invisibleGround = createSprite(200,190,400,10);
           invisibleGround.visible = false;
             //is not visible but trex stands on this.
           
           
         }
         
         function draw() {
           background(180); 
           
           //To make the trex jump while space bar is pressed and  also when y value  of  trex is above 100, which means the trex is in the lower half of the canvas.
           if(keyDown("space") && trex.y>=100) {
             trex.velocityY = -10; //giving upward velocity to make the trex jump high
           }
           // adding gravity which makes the trex come down  when the space bar is released by making the velocity positive.
           trex.velocityY = trex.velocityY + 0.8
             // we are increasing the velocity of trex to become a positive number slowly in every step so that trex comes  down on to the invisible ground.
           
           // when the ground is going out of the canvas, x value of the ground will become less than x. We have to put back the ground to the center once again.
             
           if (ground.x < 0){
             ground.x = ground.width/2;
           }
           
           trex.collide(invisibleGround);
           // this will allow  the trex to stabd on the invisible ground
          
           drawSprites();
         }
         
         
         }
         
         
         ```

         

