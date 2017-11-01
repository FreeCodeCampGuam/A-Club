# A-Club PICO-8 Puzzle
### A PICO-8 Game

#### The purpose of this game is to have a quick intro to 4 Core (Variables, Functions, Loops, and Conditionals) which will be used at the booth for A-club.

***

* **Level 1**  
    Focuses on introduction to programming with PICO-8 and variables.  

* **Level 2**  
    Focuses on functions and conditionals by having the character not move at the start and require the player to code the conditional statement for a keypress and call the function for movement.  

    The user editable code could be done like:
    ```Lua
    if btn(0) then 
        move(left)
    end

    function move(direction)
        -- code for movement with direction param
    end
    ```  

* **Level 3**  
    Focuses on showing how loops work. The puzzle could be a color game where they have to draw the same amount of blocks/sprite with a certain color using a loop.  

    For example, let's have 4 blue blocks and the player also needs to draw the same color with the same amount using a loop. Here's some pseudocode...
    User editable code:
    ```Lua
    for blue = 1,4 do
        create_blue_block()
    end
    ```  
    Logic code:
    ```Lua
    function create_blue_block()
        -- code for blue block drawing
        count_blue_block += 1
    end

    function complete_level_3()
        if count_blue_block == 4 then
            -- function for going to complete level screen
        end
    end
    ```
