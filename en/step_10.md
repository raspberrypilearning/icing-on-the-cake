## Challenge: mix up the icing

--- challenge ---

For a second challenge, let players switch between different **icing colours** — like chocolate, mint, and lemon.

--- /challenge ---

--- task ---

Make an icing chooser button: **duplicate** one of your chooser buttons and give it its own costume. Create two variables, `icing colour`{:class="block3variables"} and `counter`{:class="block3variables"}, and **untick** both. Then set the button up at the top of the stage.

![The icing chooser button costume.](images/icing-chooser.png)

```blocks3
when green flag clicked
set [counter v] to (0)
set [icing colour v] to [choc]
go to x: (166) y: (152)
```

--- /task ---

--- task ---

When the chooser is clicked, broadcast `icing` and step `counter`{:class="block3variables"} through choc, mint, and lemon.

```blocks3
when this sprite clicked
broadcast (icing v)
change y by (1)
play sound (Crank v) until done
change y by (-1)
```

```blocks3
when I receive (icing v)
change [counter v] by (1)
if <(counter) = (3)> then
set [counter v] to (0)
end
if <(counter) = (0)> then
set [icing colour v] to [choc]
end
if <(counter) = (1)> then
set [icing colour v] to [mint]
end
if <(counter) = (2)> then
set [icing colour v] to [lemon]
end
```

--- /task ---

--- task ---

Do all your cake edits on the original **cake** sprite first — it will be the chocolate one. Add these two scripts so it re-stamps when chocolate is chosen.

![The cake sprite.](images/choose-cake.png)

```blocks3
when I receive (icing v)
switch costume to (layer type)
if <(icing colour) = [choc]> then
erase all
go to x: (0) y: (0)
stamp
end
```

```blocks3
when I receive (layer v)
switch costume to (layer type)
if <(icing colour) = [choc]> then
next costume
erase all
go to x: (0) y: (0)
stamp
set [layer type v] to (costume [number v])
end
```

--- /task ---

--- task ---

Now **duplicate** the **cake** sprite for each new colour and rename the copies, like **mint cake** and **lemon cake**. The scripts come with them.

![The three cakes with chocolate, mint, and lemon icing.](images/different-cakes.png)

--- /task ---

--- task ---

For each new cake, recolour its costumes in the paint editor (green for mint, yellow for lemon), then change `choc` to its own colour in both scripts.

![Recolouring a cake costume for a new icing colour.](images/recolour-cake.gif)

--- /task ---

--- task ---

Finally, on the **toppings** sprite, copy the `touching color`{:class="block3sensing"} check in its stamping script and add one for each new colour, so toppings stamp on every cake.

--- /task ---

**Test:** Click the green flag and switch the icing. You can decorate every colour!

--- save ---
