## Cambia topping

In questo passaggio, farai cambiare costume ai tuoi **toppings** così, con un clic su un pulsante, cambierà la decorazione che stamperai.

> [!TASK]
>
> ![Lo sprite toppings.](images/sprite-toppings.png){:width="150px"}
>
> Nello sprite **toppings**, aggiungi un blocco `quando ricevo`{:class="block3events"}. Questo `passa al costume`{:class="block3looks"} corrispondente.
>
> ```blocks3
> when I receive (strawberry v)
> switch costume to (strawberry v)
> ```

> [!TASK]
>
> ![Lo sprite toppings.](images/sprite-bowbutton.png){:width="150px"}
>
> Ora crea un pulsante per ognuna delle tue decorazioni. **Duplica** lo sprite del tuo pulsante e crea un'icona modificandone l'aspetto.
>
> ![Duplicazione di uno sprite di un pulsante.](images/sprite-duplicate.png){:width="250px"}

> [!TASK]
>
> Spostare ogni pulsante in una posizione diversa lungo la parte superiore.
>
> ![Nuovo pulsante sullo stage.](images/new-button.png){:width="450px"}

> [!TASK]
>
> Modifica il messaggio `invia a tutti`{:class="block3events"} in modo che corrisponda al nome del topping.

> [!TASK]
>
> ![Lo sprite toppings.](images/sprite-toppings.png){:width="150px"}
>
> Torna sullo sprite **toppings**, duplica il blocco `quando ricevo`{:class="block3events"} per ciascuno dei tuoi nuovi pulsanti e abbina ogni messaggio al suo costume.
>
> ![Duplicazione del blocco "quando ricevo" per ogni pulsante.](images/dup-receive.gif){:width="450px"}

**Test:** Clicca sulla bandierina verde e scegli un topping, poi clicca sulla torta per stamparlo. Ora hai un decoratore di torte funzionante!

![Il decoratore di torte semplice finito.](images/finished-simple.gif){:width="450px"}

