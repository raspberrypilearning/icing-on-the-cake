## Challenge - make different cake types

You've built a full cake decorator. For a challenge, can you let the player switch between different **cake types** — different shapes and styles of cake — with a button?

--- challenge ---

--- task ---

Can you add a cake-type button that switches between different cakes each time it's clicked?

Here's one way to do it. Work through a bit at a time and test as you go.

--- /task ---

--- /challenge ---

--- collapse ---
---
title: Make a cake-type button
---

**Duplicate** one of your chooser button sprites. Change its costume so it looks different from the topping choosers — for example, a small cake symbol — so players know it changes the cake.

![A cake-type chooser button with its own symbol.](images/cake-type-button.png)

Move it to a free spot along the top of the stage.

```blocks3
when green flag clicked
go to x: (91) y: (149)
```

When it's clicked, broadcast a new `layer` message with the usual press animation.

```blocks3
when this sprite clicked
broadcast (layer v)
change y by (1)
play sound (Crank v) until done
change y by (-1)
```

--- /collapse ---

--- collapse ---
---
title: Make different cakes
---

Select the `cake` sprite and click the **Costumes** tab. Right-click your cake costume and choose **duplicate**, then change the copy into a different cake — a different shape, a taller cake, or a new decoration. Make as many as you like.

![Duplicating the cake costume and editing it into a different cake.](images/different-cakes.png)

Keep the main colour of every cake costume the **same** as your first cake, or your toppings will stop stamping on it.

--- /collapse ---

--- collapse ---
---
title: Stamp the cake types
---

Create a variable called `layer type` and **untick** it to hide it. It remembers which cake costume is showing.

On the `cake` sprite, set `layer type` to `1` at the start of its green-flag script.

```blocks3
when green flag clicked
+set [layer type v] to (1)
hide
go to x: (0) y: (0)
stamp
```

Then add a script so that when the cake receives the `layer` message, it switches to the next cake and stamps it.

```blocks3
when I receive (layer v)
switch costume to (layer type)
next costume
erase all
go to x: (0) y: (0)
stamp
set [layer type v] to (costume [number v])
```

--- /collapse ---

**Test:** Click the green flag, then click your cake-type button. The cake changes to the next one each time.

--- save ---
