## 1. Coding basics

1. creating classes, the blue prints for the objects

   ```javascript
   class myclass{
   constructor(){
   
   }
   
   myfunction(){
   
   }
   }
   ```

   2. passing values to the  constructor so that we can have  more generalised classes

      ```javascript
      class myclass{
      constructor(a,b,c,d){
      
      }
      
      myfunction(){
      
      }
      }
      ```

      

3.  creating objects from classes where ever needed.

   

   ```javascript
   sketch.js
   
   function setup(){
       myobject = new myclass(10,20,30,40); // constrcutor can take 4 values so we need to provide them here while creating the object
   }
   ```

   4. Inheritance - Parent and child relation

      We have a parent class and many child  classes which will inherit or take everything from the parent. 

      This will enable us to avoid rewriting the entire code in all the classes when  there is  so much repetition.

      keywords used:

      extends and  super

      ```javascript
      baseclass.js
      class baseclass{
      constructor(){
      
      }
      myfunction(){
      
      }
      }
      ```

      

   ```javascript
   childclass1.js
   class childclass1 extends baseclass{
       //if the constructor is  same  then just use super
       constructor(){
         super();
         //write extra lines if any needed
       }
       
       mychildfunction(){
           super.myfunction()
           //write extra lines if any needed
       }
       
   
   }
   ```

   