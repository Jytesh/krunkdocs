## Introduction

You can check/listen for user inputs. This information is useful when creating custom movement or user interacions.

<br><br/>

## Keyboard Inputs

You can check if a certain keyboard key is pressed by using KrunkScript:

<p class="hidep"><strong class="client-side">client-side</strong></p>

```krunkscript
# must be inside update loop
action update(num delta) {
    if (GAME.INPUTS.keyDown("W")) {
        # do something
    };
};
```

<br><br/>

## Mouse Position

You can get the Mouse Position at any time on the client by using KrunkScript:

<p class="hidep"><strong class="client-side">client-side</strong></p>

```krunkscript
# get mouse position on screen
obj posNormal = GAME.INPUTS.mousePos();
# do something with it

# draw red circle at mouse position on overlay
obj posOver = GAME.INPUTS.mousePosOverlay();
GAME.OVERLAY.drawCircle(pos.x, pos.y, 10, 10, 0, "#ff0000");
```

<br><br/>

## Mouse Movement

You can also get the amount the mouse has moved by this frame using KrunkScript:

```krunkscript
# get mouse movement vector
obj pos = GAME.INPUTS.mouseMovement();
```

<br><br/>

## Unlock Mouse

You unlock the mouse to allow players to interact with custom UI by using KrunkScript:

```krunkscript
# unlock mouse
GAME.INPUTS.unlockMouse();
```

To relock the mouse, players can just click off of the custom divs.

---

You can also permanently unlock your mouse if your game requires it:

```krunkscript
# unlock mouse at all times
GAME.INPUTS.freeMouse();
```

<br><br/>

## Input Listeners

The client.krnk script also has a few pre-built actions that listen for inputs events:

<p class="hidep"><strong class="client-side">client-side</strong></p>

```krunkscript
# mouse click listener
action onMouseClick(num x, num y) {
	# called every mouse click
	# do something with x & y coordinates
}

# key press listener
action onKeyPress(str key) {
    # check for key value:
    if (key == "w") {
        # pressed W
    };
}

# key up listener
action onKeyUp(str key) {
    # check for key value:
    if (key == "w") {
        # released W
    };
}

# key held listener
action onKeyHeld(str key) {
    # check for key value:
    if (key == "w") {
        # holding W
    };
}

# mouse scroll listener
action onMouseScroll(num dir) {
	# scroll direction
}
```

<br><br/>

