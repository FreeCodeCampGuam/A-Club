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
    Let's start with the first one, `__init` this is where you set up stuff. Other parts of the code are ran over and over, they are what you call **Game Loops.**  

    Let's talk about that later, first we need to start the game but there's something preventing us to do just that.

    > **_Tips:_** to `**run**` your game, use the keyboard shortcut <kbd>Ctrl</kbd>+<kbd>R</kbd>  
    
    This is a variable... 
    ```lua
    t = 0
    ```
    it's just something that holds values. What it holds can vary, hence vary...able!
    We'll use `**t**` to track how much time passed.  

* **Level 1**  

    Variables can also hold `True` or `False`
    Now let's make our game work! Let's change the variable `**start**` to something that makes our game start. What's the opposite of `False`?
    ```lua
    start = true
    ```
    Yes! Good Job!
    Now let's `**run**` our game!  

***  

* **Level 2**  
    
    Now that our game is working, we should name our game too!
    Variables can also hold words or `strings`. In PICO-8 we need to enclose our strings with quotation marks `" "`.
    Now, let's change the `**title**` variable to the name of your choice!
    ```lua
    title = "untitled"
    ```
    Got it? Let's `**run**` our game again.
    Nice!  

***  

* **Level 3**
    