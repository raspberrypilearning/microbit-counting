L'une des choses que tu pourrais demander à un utilisateur est de stocker le comptage !

### Créer une variable

Tout d'abord, tu as besoin d'une variable pour stocker ton comptage.

Ouvre le menu `Variables`{:class='microbitvariables'} et clique sur **Créer une variable**.

Donne un nom logique à ta variable, par exemple le sujet de ton comptage.

### Définir la variable au début

Quand ton programme commence, tu veux que la variable soit définie à `0`.

Ouvre le menu `Variables`{:class='microbitvariables'} dans la boîte à outils et fais glisser un bloc `définir`{:class='microbitvariables'} dans ton bloc `au démarrage`{:class='microbitbasic'}.

```microbit
let mouvements = 0
```

### Augmenter la variable

Ensuite, tu dois décider **quand** tu veux que le nombre augmente.

Tu peux utiliser des **événements** pour augmenter la variable, comme un bloc `lorsque le bouton est pressé`{:class='microbitinput'}.

```microbit
let mouvements = 0
input.onButtonPressed(Button.A, function () {
    mouvements += 1
})
```

Tu peux aussi compter quand une **condition** est remplie, comme tu l'as fait dans [Suivi du sommeil](https://projects.raspberrypi.org/fr-FR/projects/sleep-tracker){:target="_blank"}:

```microbit
let mouvements = 0
basic.forever(function () {
    if (input.rotation(Rotation.Roll) < -10 || input.rotation(Rotation.Roll) > 10) {
        mouvements += 1
    }
})
```
