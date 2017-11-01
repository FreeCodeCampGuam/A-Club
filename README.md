# A-Club PICO-8 Puzzle
### A PICO-8 Game

#### The purpose of this game is to have a quick intro to 4 Core (Variables, Functions, Loops, and Conditionals) which will be used at the booth for A-club.

***

- [ ] **Level 1**  
    Focuses on introduction to programming with PICO-8 and variables. The section for variables should show the player that variables can contain strings, numbers, and boolean.  

    The variables could be done like so:  

    | Variable Type | User Input | Example |
    | --- | --- | --- |
    | String | Name | `name = bob` |
    | Number | Age or Color Choice | `favorite_color = 00` |
    | Boolean | Game Start | `start_game = false` |
  

- [ ] **Level 2**  
    Focuses on functions and conditionals by having the character not move at the start and require the player to code the conditional statement for a key press and call the function for movement.  

    The user editable code could be done like:
    ```Lua
    if btn(0) then 
        move(left)
    end

    function move(direction)
        -- code for movement with direction param
    end
    ```

- [ ] **Level 3**  
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
- [ ] **Level 4 and up**  
    These levels could focus on solving problems with the other tools in PICO-8 including the sprite sheet, map editor, and sfx.  

    Example activities that could be done here:
    1. Choosing a character from the sprite sheet with a variable and [optional] quick customization of their character.
    2. Solving how to get through a certain part of the map with an unaccessible key/door by adding "solid" sprites.
    3. Finding where the key for the door is using 3 sfx sounds for 3 proximities such as "Near, Close, and On Top of the Key, `Press X`."  