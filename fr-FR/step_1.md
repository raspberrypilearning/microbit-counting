One of the things you might want a user to be able to do is keep count!

### Create a variable

First, you need a variable to hold your count.

Open the `Variables`{:class='microbitvariables'} menu and click **Create a Variable**.

Give your variable a meaningful name, such as the thing you are counting.

### Set the variable at the start

When your program begins, you want the Variable to be set to `0`.

Open the `Variables`{:class='microbitvariables'} menu in the Toolbox and drag a `set`{:class='microbitvariables'} block into your `on start`{:class='microbitbasic'} block.

```microbit
let movements = 0
```

### Increase the variable

Next, you need to decide **when** you want the count to increase.

You can use **events** to increase the variable, like an `on button pressed`{:class='microbitinput'} block.

```microbit
let movements = 0
input.onButtonPressed(Button.A, function () {
    movements += 1
})
```

You might also want to count when a **condition** is met, like you did in [Sleep tracker](https://projects.raspberrypi.org/en/projects/sleep-tracker){:target="\_blank"}:

```microbit
let movements = 0
basic.forever(function () {
    if (input.rotation(Rotation.Roll) < -10 || input.rotation(Rotation.Roll) > 10) {
        movements += 1
    }
})
```
