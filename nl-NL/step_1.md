Eén van de dingen die je een gebruiker zou kunnen laten doen is het bijhouden van een telling!

### Maak een variabele

Eerst heb je een variabele nodig om de telling bij te houden.

Open het Variabelen{:class="microbitvariables"} menu en klik op **Maak een variabele**.

Geef je variabele een logische naam, zoals het onderwerp van je telling.

### Stel de variabele aan het begin in

Wanneer je programma start, wil je dat de variabele op `0` gezet wordt.

Open het `Variabelen`{:class='microbitvariables'} menu in de Toolbox en sleep een `stel in op`{:class='microbitvariables'} blok naar je `bij opstarten`{:class='microbitbasic'} blok.

```microbit
let movements = 0
```

### Verhoog de variabele

Vervolgens moet je beslissen **wanneer** je wilt dat de telling stijgt.

Je kunt **gebeurtenissen** gebruiken om de variabele te verhogen, zoals een `wanneer knop wordt ingedrukt`{:class='microbitinput'} blok.

```microbit
let movements = 0
input.onButtonPressed(Button.A, function () {
    movements += 1
})
```

Je wilt misschien ook tellen wanneer aan een **voorwaarde** is voldaan, zoals je deed in het project [Slaap monitor](https://projects.raspberrypi.org/en/projects/sleep-tracker){:target="_blank"}:

```microbit
let movements = 0
basic.forever(function () {
    if (input.rotation(Rotation.Roll) < -10 || input.rotation(Rotation.Roll) > 10) {
        movements += 1
    }
})
```
