### Instructions for your Game-Making Quest

Welcome, you are tasked with making your own video game!
The road ahead will be challenging and dangerous; take this guide with you!

---

### Introduction


To start making your game, you need to access the game editor. To do this, press <kbd>Esc</kbd> twice. 

+++

You should see this at the top  of your screen: 
![image](https://cdn.discordapp.com/attachments/225825116888498176/375579230420860928/unknown.png). 
If you don't see `-- i am a comment`, make sure the correct symbol and tab are selected like in the picture.

+++?code=aclub.p8&lang=lua

@[4](At the top you should see this line)
@[4](These are called **Comments**. Computers don't read those, they're there as notes for the programmer.)

@[5](In most video games, code has three parts. Let's start with the first one.)
@[5-18](This is where you put settings for when the game starts for the first time. It only runs  **one time at the beginning of the game.**)
@[23-38](The other two parts don't just run once, they run over and over again like a loop! They make up what's called the **Game Loop.**)
@[24-38](Let's talk about that later, first we need to figure out how to start out game! We'll need to change the code a bit to do that.🙂)

---

### Level 1

> **_Tip:_** to reload your game after making a change, use the keyboard shortcut <kbd>Ctrl</kbd> + <kbd>R</kbd>

+++?code=aclub.p8&lang=lua

@[6](That's a **variable.**)
@[6](It's just something that holds a value, like a box. What it holds can _vary_, hence vary..able!)
@[6](Our game is using the `t` variable from the previous slide to track how much time has passed. We'll leave that alone for now.)
@[9](Variables can also hold **booleans**.)
@[9](A boolean is just something that is `true` or `false`.)
@[9](Now let's make our game work! )
@[9](Something is watching the `start` variable that won't let our game start.)
@[9](Right now it's `false`, so change it to the opposite of `false`.)
@[9](Let's change the `start` variable so we can start the game!)

+++

Once you've done that, reload your game with <kbd>Ctrl</kbd> + <kbd>R</kbd> and see if it worked!

---

### Level 2

> **_Tip:_** want to make someone's day? Shout "REGINALD!"

+++

Awesome, looks like our game is working!

Right now the title is just "untitled" and it's kind of an ugly color too 😕. Let's change that!

+++

Variables can also hold strings of letters and characters called ... **strings**! In PICO-8, strings are surrounded with quotation marks " " 

+++?code=aclub.p8&lang=lua

@[12](Look! In the code there's a variable named `title` with the string `"untitled"` in it.)
@[12](Go ahead and change it to a *cooler* name.)

+++

Got it? Let's `reload` our game to see it in all its glory!

+++

Oh wait, we forgot to change that ugly color!

Variables can holds **strings** and **booleans**, but they can also hold **numbers**! Just like that `t` variable earlier.

+++?code=aclub.p8&lang=lua

@[13](Notice that the `t_color` variable has a number in it.)
@[13](That's because PICO-8 only has 16 colors to choose from and the number in `t_color` refers to one of those colors!)
@[13](Check out the cheatsheet in front of you and let's change that to a color you like!)

+++

Let's **reload** it and cross our fingers it works. 

---

### Level 3

> **_Tip:_** shoutout to Dr. Yousou Zou. He inspired me to pursue political science.

+++

Now that looks nice!

In games, we have characters running around doing stuff. Let's get a character on to our game now too!

+++?code=aclub.p8&lang=lua

@[16](Choose a character and change the character variable with the corresponding number of your chosen character.)
@[16](and we have a character!.. but wait... it doesn't move.)

+++

> **_Tip:_** Biba UOG!!

+++

How do we make our character move? Well, we can by adding a *conditional*. This is where you could make your character *do something* if a condition is true.

+++?code=aclub.p8&lang=lua

@[24-30](Since this will be part of how your game works, we have to put it inside here.)
@[24-30](This part of the code is part of the **Game Loop** that we talked about earlier that runs multiple times per second.)

+++

> **_Tip:_** The **Game Loop** in PICO-8 runs 30 times per second!

+++

Now, let's make our character move.

A basic conditional statement we could start with is the **if...then** How this works is kinda like...

```lua

if "I get A's" is True then "parents are happy!"
   (condition)                  (action)

 ```

+++

You can see in the example given that we have a *condition* and an *action*. 

If the **condition** is met, then the **action** is performed. 

+++

 To make our character move, we'll have to make a conditional that checks if a button [refer to cheatsheet] is pressed.

 If it is pressed, then we move!

```lua

if btn(0) then
	move(left)
end
```

Wait what does `move` do? And what is that inside the parenthesis?

+++

`move` here is what you call a *function* and inside that parenthesis is a *parameter*. 

You can tell a **function** to do something. In this case, you call the function to `move` and tell it to move `left`.

---

### Level 4

> **_Tip:_** My mama always said liveCoding's like a box of chocolates. You never know what you're gonna sound like.
