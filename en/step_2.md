## Make a topping

In this step, you'll make your first **topping**. 

--- task ---

Start a [new Scratch project](https://scratch.mit.edu/projects/editor/){:target="_blank"}.

--- /task ---

--- task ---

Delete the cat sprite.

![Deleting the cat sprite with the trashcan.](images/delete-cat.png)

--- /task ---

--- task ---

Add a new sprite for your topping. Hover over **Choose a Sprite** and pick **Paint** to draw your own, or choose one from the library.

![The Choose a Sprite menu.](images/choose-sprite.png)

A topping can be anything you like — sprinkles, a strawberry, a bow, or a candle. 

--- /task ---

--- task ---

Name the sprite **toppings**, because later it will have lots of different toppings. 

In the box, delete "Sprite1" and type "Toppings".

![Renaming the sprite to toppings.](images/rename-sprite.png)

--- /task ---

--- task ---

Make the sprite follow the cursor using a `go to`{:class="block3motion"} block.

```blocks3
when green flag clicked
forever
go to (mouse-pointer v)
end
```

--- /task ---

--- task ---

Now make it draw a topping when you click.

Find the **stamp** block by clicking the **Add Extension** in the bottom-left corner, then choose **Pen**.

![Adding the Pen extension.](images/pen-extension.gif)

--- /task ---

--- task ---

Add an `if then`{:class="block3control"} block inside the `forever`{:class="block3control"} loop that checks `mouse down?`{:class="block3sensing"} and then it **stamps**.

```blocks3
when green flag clicked
forever
go to (mouse-pointer v)
+if <mouse down?> then
stamp
end
end
```

--- /task ---

**Test:** Click the green flag and click around the stage. Your topping should stamp wherever you click.

--- task ---

Choose a sound for each time you add a topping from the sound library.

First add a new sound in the **Sounds tab**. Then add a `play sound until done`{:class="block3sound"} block and select your sound from the drop-down menu.

![The Sounds tab, where you add a new sound.](images/sounds-tab.png)

```blocks3
when green flag clicked
forever
go to (mouse-pointer v)
if <mouse down?> then
+play sound (Pop v) until done
stamp
end
end
```

--- /task ---

**Test:** Click the green flag, then click around the stage to see stamps of your topping. Test that they erase when you click the green flag again.
