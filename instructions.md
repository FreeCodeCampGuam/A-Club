#Instructions on how to play the A-Club PICO-8 Puzzle

#### Follow the instructions carefully and do the steps one by one to ensure you are progressing correctly.

***

##### Welcome! In this exercise you will be making a game at the same time learning about the basics of programming. What are you waiting for? Let's get to it!

* **Introduction**  
    To start making your game, you need to access the game editor.
    You need to press <kbd>Esc</kbd> twice (<kbd>Esc</kbd>, <kbd>Esc</kbd>)  
    
    Once you are in the editor, you should see in the very first line: 
    ```lua
    --I am a comment
    ```

    They are called comments. Computers don't read those, it's there to give notes to other programmers.  

    In most video games, code is separated into three parts.  
    Let's start with the first one...
    ```lua
    function __init()

    end
    ```
    This is where you set up stuff. Other parts of the code are ran over and over, they are what you call **Game Loops.**  

    Let's talk about that later, first we need to start the game but there's something preventing us to do just that.

    > **_Tips:_** to **`run`** your game, use the keyboard shortcut <kbd>Ctrl</kbd>+<kbd>R</kbd>  
    
    This is a *variable*... 
    ```lua
    t = 0
    ```
    it's just something that holds values. What it holds can vary, hence vary...able!
    We'll use **`t`** to track how much time passed.  

* **Level 1**  

    Variables can also hold `True` or `False`
    Now let's make our game work! Let's change the variable **`start`** to something that makes our game start. What's the opposite of `False`?
    ```lua
    start = true
    ```
    Yes! Good Job!
    Now let's **`run`** our game!  

***  

* **Level 2**  
    
    Now that our game is working, we should name our game too!
    Variables can also hold words or `strings`. In PICO-8 we need to enclose our strings with quotation marks `" "`.
    Now, let's change the **`title`** variable to the name of your choice!
    ```lua
    title = "untitled"
    ```
    Got it? Let's **`run`** our game again.
    Nice!  

***  

* **Level 3**  
    
    Now our game runs and has a title. But, that title color doesn't feel right.   
    Variables can also hold numbers and since PICO-8 has 16 colors [refer to cheatsheet]. We can choose another color and use that instead!
    ```lua
    t_color = 2
    ```
    After you are done editing, **`run`** the game again to see if it works.
    Now, that looks fancy!  

***  

* **Level 4**  
    
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

***  

* **Level 5**
