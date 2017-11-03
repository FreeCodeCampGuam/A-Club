__#__ Instructions for your Game-Making Quest

You are tasked with making your own video game!  
The road ahead will be challenging and dangerous; take this guide with you!

#### Follow the instructions carefully and do the steps one by one to ensure you are progressing correctly.

***

##### Welcome! In this exercise you will be making a game at the same time learning about the basics of programming. What are you waiting for? Let's get to it!

* **Introduction**  
    To start making your game, you need to access the game editor. To do this, press <kbd>Esc</kbd> **twice**.
    
    You should see this at the top of your screen:  
    ![image](https://user-images.githubusercontent.com/17536161/32310549-d306ebb2-bfde-11e7-9f03-1d329887805b.png)
    
    You should see this on the very first line:
    ```lua
    -- i am a comment
    ```
    These are called comments. Computers don't read those, they're there to give notes to other programmers.  
    
    If you don't see `-- i am a comment` on the very first line, make sure to click the left-most symbol on the top-right of your screen ![image](https://user-images.githubusercontent.com/17536161/32310648-9d782258-bfdf-11e7-9eae-495276b19fa9.png). This is your **code editor**. 

    In most video games, code is separated into three parts.  
    Let's start with the first one...
    ```lua
    function __init()

    end
    ```
    This is where you set up stuff. It's run only one time at the beginning of the game. 
    The other two parts are ran over and over, they make up what's called the **Game Loop**.  

    Let's talk about that later, first we need to figure out how to start our game. We'll need to change the code a bit to do that.

* **Level 1**  

    > **_Tip:_** to **`reload`** your game after making a change, use the keyboard shortcut <kbd>Ctrl</kbd>+<kbd>R</kbd>  
    
    In your `__init`, you should see
    ```lua
    t = 0
    ```
    That's a **variable**.  
    it's just something that holds a value. What it holds can vary, hence vary...able!  
    Our game is using the **`t`** variable to track how much time has passed. We'll leave that alone for now.

    Variables can also hold **booleans**. A boolean is just something that is `true` or `false`.  
    Now let's make our game work! Something is watching the `start` variable and stopping our game from running. Let's change the **`start`** variable so that we can start the game. Right now it's `false`, so change it to the opposite of `false`!

    Once you've done that, reload your game with <kbd>Ctrl</kbd>+<kbd>R</kbd> and see if it worked!
    
***  

* **Level 2**  

    Awesome, looks like our game is working!  
    
    Right now the title is just "untitled" and it's kind of an ugly color too 😕. Let's change that!  
    
    Variables can also hold strings of letters and characters called... **strings**! In PICO-8, strings are surrounded with quotation marks `" "` to tell the computer that we want to use the "literal" characters between the quotes.  
    
    Look! In the code, there's a variable named `title` with the string `"untitled"` in it. Let's change that to a *cooler* name.
    
    Got it? Let's **`reload`** our game to see it in all its glory.

    Oh wait, we forgot to change that ugly color!
    
    Variables can hold **strings** and **booleans**, but they can also hold **numbers**! Just like that `t` variable earlier.
    
    Notice, the `t_color` (title color) variable has a number in it. That's because PICO-8 only has 16 colors to choose from, and the number in `t_color` refers to one of those colors!

    Check out the cheatsheet in front of you and let's change that to a color you like!
    
    Let's **reload** it an cross our fingers it works. 🤞

***  

* **Level 3**  

    Now that looks nice! 
    
    In games, we have characters running around doing stuff. Let's get a character on to our game now too!  
    Choose a character and edit the character variable with the corresponding number of the character of your choice.
    ```lua
    character = 01 
    ```
    and we have a character! but wait... it doesn't move.  

    We can fix that by adding adding a *conditional*. This is where you could do decision making inside your game.  
    Since this will be part of how your game works, we have to put it inside 
    ```lua
    function __update()

    end
    ```
    This part of the code is **Game Loop** that we talked about earlier that runs multiple times per second.
    > **_Tips:_** The **Game Loop** in PICO-8 runs 30 times per second!  
    
    Now on the conditionals, let's make our character move~
    A basic conditional statement we could start with is the **`if...then`**
    How this works is kinda like...
    ```lua
    if "I get A's"  is True then "parents are happy!"
       (conditional)             (action)
    ```
    You can see here we have a _conditional_ and an _action_ if the **condition** is met, hence condition...al :)  

    To make our character move, we'll have to do a conditional that checks if a button [refer to cheatsheet] is pressed then we move.
    ```lua
    if btn(0) then
        move(left)
    end
    ```
    Wait, what does **`move`** do? And what is that inside the parenthesis??
    **`move`** here is what you call a *function* and inside that parenthesis is a *parameter*. It's more code somewhere else and you can tell it to do something. In this instance you *call* the function **`move`** and tell it to do move **`left`**. 
    
    Now let's do the same for **`right`**, same thing as doing it for left but going right this time.

    Alright, so we got some movement logic down, let's move on over to drawing stuff. For that we go to 
    ```lua
    function _draw()

    end
    ```

    First, we gotta draw the map, we can do so by calling the function `draw_map()`
    Hmm... where is our character? Oh right, we have not called the function for that one either. Let's do it by doing `draw_player()`

    Now, try it out by reloading!

    Oh no! It doesn't work, we must be forgetting something...
    Ah right, `draw_player()` needs parameters too like our cool friend `move()` but this time it is structured like this `draw_player(px, py)`  

    You don't write in `px` and `py`, you replace them with where you want to place your player character when it's drawn! Refer to the cheatsheet for details on how to use PICO-8's coordinate plane (or have it on screen)

***  

* **Level 4**  

    Look! there's a door on the map!
    You probably saw the switch in the sprite sheet, if not check it out!
    We'll be using the switch to open the door. Let's spawn in that switch with `draw_switch(x)` and you guessed it, it'll have to go under the `_draw()` function (can show these with code-presenter easier)
    Don't forget to fill in that parameter! That paremeter asks for where you want to put that swtich on, only between (1-15).

    Great! Now we have a switch but we can't do anything with it now can we? Let's add in another conditional to look for when you press an action key, say <kbd>Z</kbd> same thing you did with `move()` but this time with `hit_switch()` (assuming they did the move conditionals already, show the "correct answer" for move as reference with code-presenter).

    Hmm... something looks wrong, there are holes on the ground. How will we get to the door?

    Luckily, we're in a code editor. To solve that problem, we'll have to make our bridge.  

    You've used **`functions`** before, this time we will have you make one!
    
    So this how you will have to structure your **`function`** 
    ```lua
    function insert_function_name_here()

    end
    ```
    (Do fancy code-presenter here to explain what `function` is and what `inser_function_name_here` is. Remind them to not forget the parentheses.)
    (another fancy code-presenter for `end` to show that all functions are enclosed like this)

    Now you have constructed a "house" for your function, you gotta fill it with your code for bridge building.  

    We'll give you some hints on how to do this.
    First, we'll have to use **`loops`** this is different from **`Game Loops`** as you can control how often these loops run. For instance (heh) we could use a **`For...loop`** and here is how it is structured:

    ```lua
    for n =         1,       10   do
        (variable)  (start) (stop)

        draw_cat()
        (action)
    end
    ```

    (Code-presenter: explain what the for loop starts with something like "This sets a variable named `n` to be `1` at the **start** of the loop and continues executing the **action** where the code you want to run the amount of times until you tell it to **stop** at that number.")
    (This will execute the code `draw_cat()` 10 times (1,2,3, ... ,10))
    (**`Loops`**, in this case a **`For...loop`**, ends with... `end`!)

    Now, let's really build that bridge. Here are some steps to follow:
    1. Create a **`function`** for your bridge building shenanigans
    2. Create a loop, (**_Hint:_** `For...loop`) that builds bridges for the amount of tiles the **floor is missing**.
    3. **Add tiles** to fill in the floor by calling up another function. Don't forget to put this inside your **`For...loop`**!