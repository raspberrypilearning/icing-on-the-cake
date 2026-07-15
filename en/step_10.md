## Challenge: add new flavours

--- challenge ---

For a second challenge, let players switch between different **flavours** of cake — like chocolate, mint, and lemon — each a different colour.

--- /challenge ---

--- task ---

**Duplicate** your **cake** sprite once for each new flavour, and rename the copies, like **mint cake** and **lemon cake**.

![The three flavour cakes: chocolate, mint, and lemon.](images/different-cakes.png)

--- /task ---

--- task ---

In the **Costumes** tab, recolour each cake to match its flavour — for example, yellow for lemon and green for mint.

![Recolouring a cake costume for a new flavour.](images/recolour-cake.gif)

--- /task ---

--- task ---

Create two variables, `counter`{:class="block3variables"} and `icing colour`{:class="block3variables"}, and **untick** both to hide them.

--- /task ---

--- task ---

**Duplicate** a chooser button for the flavours, and set it up to start on chocolate at the top of the stage.

![The icing chooser button costume.](images/icing-chooser.png)

```blocks3
when green flag clicked
set [counter v] to (0)
set [icing colour v] to [choc]
go to x: (166) y: (152)
```

--- /task ---

--- task ---

When it's clicked, broadcast `icing` with the usual press animation.

```blocks3
when this sprite clicked
broadcast (icing v)
change y by (1)
play sound (Crank v) until done
change y by (-1)
```

--- /task ---

--- task ---

Make each click move to the next flavour, using `counter`{:class="block3variables"} to step through choc, mint, and lemon.

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

On each flavour cake, add scripts so it only stamps when its flavour is chosen. This is the **mint cake** version — change `mint` to match each cake.

```blocks3
when I receive (icing v)
switch costume to (layer type)
if <(icing colour) = [mint]> then
erase all
go to x: (0) y: (0)
stamp
end
```

```blocks3
when I receive (layer v)
switch costume to (layer type)
if <(icing colour) = [mint]> then
next costume
erase all
go to x: (0) y: (0)
stamp
set [layer type v] to (costume [number v])
end
```

--- /task ---

--- task ---

Your **toppings** sprite only checks for the first cake's colour. In its stamping script, copy the `touching color`{:class="block3sensing"} check and add one for each flavour's colour, so toppings stamp on every cake.

--- /task ---

**Test:** Click the green flag and switch flavours. You can now decorate any of them!

--- save ---
