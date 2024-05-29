# 10.3.10-Marvel-Game
Graded

## Part 1 - Adding the Button Code for the Existing Characters (60%)

1. Each scene has buttons created for you that currently do not work.  You will notice that the buttons are all in different places. This is deliberate and should not be changed.
2. Although it does not say in the instructions for the user, pressing Y or N on the first scene will advance you to the next scene. Eventually you should remove this code but it is left there as an example to remind you what the buttons should do.
3. Your task is to add the `IF` statements into the `MousePressed` function so that all the buttons work:
    - You are allowed to ask for help from classmates or your teacher for the first 2 scenes. 
    - You may NOT ask for  help on scenes 3 and 4 so make sure you LEARN when getting help on the first 2
    - Be sure to add the 	`&& scenenum===` 	to the `IF` statement.



## Part 2 - Adding to the Existing Characters OR Changing the theme (20%)

You have 2 options for this part of the assignment:

### Option 1 - Change the Theme
Alter the theme to be something you are more interested in. It could still be fictional characters, could be historical figures, famous Computer Scientists, or parts of a computer or car.  Anything goes!

There are 7 characters that work in the Start Code. Alter the variable names, questions and answers so that it works for 7 answers in your new theme.


### Option 2 - Stay with the Marvel Theme but Add More Characters
Add 4 more characters to our example. This should bring you to ELEVEN characters in total.  
Add any necessary new variables.
Then add the questions necessary for those variables.
Then add the new boolean AND statements to your end scene.
 

## Part 3 Final 20% - Title Page

Both parts of this task must be completed to earn any marks.

1. Add a title page. This should act as scene ZERO.  On the title page::
Print a title for your game
2. Tell the user which characters to choose from. In other words, move this from scene1.

Create a `CIRCULAR` button that says `BEGIN`
Then look up how the dist() function works on the https://p5js.org/reference/ and/or other help sources.
Use the `dist()` function and the radius of your button in a new `IF` statement so that clicking on the circle moves you to scene 1.



```

//Ironman, Groot, Spiderman, Wanda, Black Widow, Loki, Nebuba
let scenenum = 1;
let isHuman = false;
let isFemale = false;
let isAnimal = false;
let isGod = false;

function preload() {

}//end preloading of images and fonts

function setup() {
    createCanvas(600, 400);
    background(255, 255, 0);
}//end setup

function draw() {

    if (scenenum === 1) {
        scene1();
    } else if (scenenum === 2) {
        scene2();
    } else if (scenenum === 3) {
        scene3();
    } else if (scenenum === 999) {
        endscene();
    } else if (scenenum === 4) {
        scene4();
    } 
}//end draw



function mousePressed() {
    print("MouseX: " + mouseX +"     MouseY: " + mouseY  );

  if(scenenum===1 && mouseX>100 && mouseX<200 && mouseY>200 && mouseY<250){
    print("Debug: you clicked yes on question 1");
    scenenum = 2;
    isHuman = true;     //set the boolean variable equal to true when you press yes
  }

// else if(scenenum===1 && mouseX 


}//end mousePressed

function scene1() {
    background(255, 255, 0);
    textSize(14);
    fill(0);
    noStroke();
    text("Choose one of the following characters:", 50, 60);
    text("Ironman, Groot, Spiderman, Wanda, Black Widow, Loki, Nebula", 50, 80);
    text("Is your character from earth?", 50, 100);

    //buttons
    fill(200);
    stroke(0);
    strokeWeight(2);
    rect(100, 200, 100, 50); //yes
    rect(300, 200, 100, 50);  //no
    textSize(14);
    fill(0);
    noStroke();
    text("YES", 130, 230);
    text("No", 330, 230);
    
}
function scene2() {
    background(255, 255, 0);
    textSize(14);
    fill(0);
    noStroke();
    text("Is your character female?", 50, 140);

    //buttons
    fill(200);
    stroke(0);
    strokeWeight(2);
    rect(100, 300, 100, 50); //yes
    rect(300, 300, 100, 50); //no
    textSize(14);
    fill(0);
    noStroke();
    text("YES", 130, 330);
    text("No", 330, 330);
}

function scene3() {
    background(255, 255, 0);
    textSize(14);
    fill(0);
    noStroke();
    text("Is your character's name related\nto an animal?", 50, 120);

    //buttons
    fill(200);
    stroke(0);
    strokeWeight(2);
    rect(200, 200, 100, 50); //yes
    rect(400, 200, 100, 50);  //no
    textSize(14);
    fill(0);
    noStroke();
    text("YES", 230, 230);
    text("No", 430, 230);
}
function scene4() {
    background(255, 255, 0);
    textSize(14);
    fill(0);
    noStroke();
    text("Is your character a God?", 50, 120);

    //buttons
    fill(200);
    stroke(0);
    strokeWeight(2);
    rect(50, 300, 100, 50);  //yes
    rect(250, 300, 100, 50);  //no
    textSize(14);
    fill(0);
    noStroke();
    text("YES", 80, 330);
    text("No", 280, 330);
}

function endscene() {
   
    background(255, 255, 0);
    textSize(14);
    fill(0);
    noStroke();
    text("Your character is... ", 50, 90);
    if(isHuman  && !isFemale && !isAnimal && !isGod){
         text("Ironman!", 50, 120);
    } else if(!isHuman  && !isFemale && !isAnimal && !isGod){
         text("Groot!", 50, 120);
    } else if(isHuman  && !isFemale && isAnimal && !isGod){
         text("Spiderman!", 50, 120);
    } else if(isHuman  && isFemale && !isAnimal && !isGod){
         text("Wanda!", 50, 120);
    } else if(isHuman  && isFemale && isAnimal && !isGod){
         text("Black Widow!", 50, 120);
    } else if(!isHuman  && !isFemale && !isAnimal && isGod){
         text("Loki!", 50, 120);
    } else if(!isHuman  && isFemale && !isAnimal && !isGod){
         text("Nebula!", 50, 120);
    } 
    //space left here for future ELSE IF statements

    else{
        text("Error - Character not found.", 50, 120)
    }

}//endscene

``` 
