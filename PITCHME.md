### Instructions for your Game-Making Quest

Welcome, you are tasked with making your own video game!
The road ahead will be challenging and dangerous; take this guide with you!

---

### Introduction


To start making your game, you need to access the game editor. To do this, press **Esc** twice. 

+++

You should see this at the top  of your screen: 
![image](https://cdn.discordapp.com/attachments/225825116888498176/375579230420860928/unknown.png)

+++

At the top you should see the line: 
```lua
	-- i am a comment
``` 

+++

These are called comments. Computers don't read those, they're there as notes for the programmer 

+++

In most video games, code has three parts. Let's start with the first one: |
```lua
    function __init()

    end
``` 
- This is where you put settings for when the game starts for the first time. It only runs  **one time at the beginning of the game.** 

- The other two parts don't just run once, they run over and over again like a loop! They make up what's called the **Game Loop.** 

+++

Let's talk about that later, first we need to figure out how to start out game! 

We'll need to change the code a bit to do that. :)

---

### Level 1

> **_Tip:_** to reload your game after making a change, use the keyboard shortcut Ctrl + R

+++

```lua
t = 0
```

That's a **variable.**

It's just something that holds a value, like a box. What it holds can _vary_, hence vary..able! 

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

Let's **reload** it and cross our fingers it works. 🤞




