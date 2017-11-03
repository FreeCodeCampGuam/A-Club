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
@[4](These are called comments. Computers don't read those, they're there as notes for the programmer.)

+++

+++code=aclub.p8&lang=lua

@[5](In most video games, code has three parts. Let's start with the first one.)
@[5-18](This is where you put settings for when the game starts for the first time. It only runs  **one time at the beginning of the game.** 

The other two parts don't just run once, they run over and over again like a loop! They make up what's called the **Game Loop.**)

+++

Let's talk about that later, first we need to figure out how to start out game! 

We'll need to change the code a bit to do that. :)

---

### Level 1

> **_Tip:_** to reload your game after making a change, use the keyboard shortcut Ctrl + R

+++code=aclub.p8&lang=lua

@[6](That's a **variable.**

It's just something that holds a value, like a box. What it holds can _vary_, hence vary..able!)

+++

Our game is using the `t` variable from the previous slide to track how much time has passed. We'll leave that alone for now.

+++

Variables can also hold **booleans**. 

A boolean is just something that is `true` or `false`.

+++

Now let's make our game work! 

Something is watching the `start` variable that won't let our game start. 

Let's change the `start` variable so we can start the game!

+++

Right now it's `false`, so change it to the opposite of `false`.

Once you've done that, reload your game with Ctrl + R and see if it worked!

---

### Level 2

> **_Tip:_** want to make someone's day? Shout "REGINALD!"

+++

Awesome, looks like our game is working!

Right now the title is just "untitled" and it's kind of an ugly color too 😕. Let's change that!

+++

Variables can also hold strings of letters and characters called ... **strings**! In PICO-8, strings are surrounded with quotation marks " " 

Look! In the code there's a variable named `title` with the string `"untitled"` in it. 

Go ahead and change it to a *cooler* name.

+++

Got it? Let's `reload` our game to see it in all its glory!

+++

Oh wait, we forgot to change that ugly color!

Variables can holds **strings** and **booleans**, but they can also hold **numbers**! Just like that `t` variable earlier.

+++

Notice that the `t_color` variable has a number in it. That's because PICO-8 only has 16 colors to choose from and the number in t_color refers to one of those colors!


Check out the cheatsheet in front of you and let's change that to a color you like!

+++

Let's **reload** it and cross our fingers it works. 

---

### Level 3

> **_Tip:_** shoutout to Dr. Yousou Zou. He inspired me to pursue political science.

+++

Now that looks nice!

In games, we have characters running around doing stuff. Let's get a character on to our game now too!

+++

Choose a character and change the character variable with the corresponding number of your chosen character.

```lua

character = 01

```

and we have a character!.. but wait... it doesn't move.

---

### Level 4

> **_Tip:_** Biba UOG!!

+++

How do we make our character move? Well, we can by adding a *conditional*. This is where you could make your character *do something* if a condition is true.

Since this will be part of how your game works, we have to put it inside:

```lua

function _update()

end

```

+++

This part of the code is part of the **Game Loop** that we talked about earlier that runs multiple times per second.

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

### Level 5

> **_Tip:_** My mama always said liveCoding's like a box of chocolates. You never know what you're gonna sound like.
