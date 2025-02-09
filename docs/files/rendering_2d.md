## Introduction

Want to show something on screen? You came to the right place. Depending on the type of game you want to make, you will either want to render 2D elements, 3D elements or both.\
For rendering 3D Objects, please refer to the [3D Objects](./files/scene?id=adding-3d-objects) or [Custom Assets](./custom_assets?id=resources) section. Any 3D object added to the scene will render automatically.

<br><br/>

## Overlay Canvas

The overlay canvas allows you to render 2D Elements on the screen. This is useful for [creating UI](./files/user_interface?id=adding-an-element-div) elements or rendering game objects for a 2D Game.

<br><br/>

## Render Loop

Krunker automatically updates every frame. To smoothly render objects put all your rendering logic inside the render action on the client:

<p class="hidep"><strong class="client-side">client-side</strong></p>

```krunkscript
# built-in render action
action render(num delta) {

    # clear overlay canvas (optional)
    GAME.OVERLAY.clear(); # do once before rendering

    # render after logic is processed
    GAME.OVERLAY.drawRect(0, 0, 0, 20, 15, 0, "#ff0000", 1); # red rectangle
}
```

<br><br/>

## 2D Shapes

Two dimensional shapes to render on overlay canvas.

___

**Rectangles**

<p class="hidep"><strong class="client-side">client-side</strong></p>

```krunkscript
GAME.OVERLAY.drawRect(
    x, # num x position on canvas
    y, # num y position on canvas
    w, # num width
    h, # num height
    r, # num rotation (degrees)
    color, # str color
    opac # num opacity
);
```

___

**Circles**

<p class="hidep"><strong class="client-side">client-side</strong></p>

```krunkscript
GAME.OVERLAY.drawCircle(
    x, # num x position on canvas
    y, # num y position on canvas
    w, # num width
    h, # num height
    r, # num rotation (degrees)
    color, # str color
    opac # num opacity
);
```

___

**Lines**

<p class="hidep"><strong class="client-side">client-side</strong></p>

```krunkscript
GAME.OVERLAY.drawLine(
    x1, # num x start position on canvas
    y1, # num y start position on canvas
    x2, # num x end position on canvas
    y2, # num y end position on canvas
    t, # num thickness
    color, # str color
    opac # num opacity
);
```

___

<br><br/>

## Other Elements

Other elements you can render on the overlay canvas.

___

**Images**

<p class="hidep"><strong class="client-side">client-side</strong></p>

```krunkscript
GAME.OVERLAY.drawImage(
    aid, # str asset id of image
    x, # num x position on canvas
    y, # num y position on canvas
    w, # num width
    h, # num height
    r, # num rotation (degrees)
    opac # num opacity
);
```

___

**Text**

<p class="hidep"><strong class="client-side">client-side</strong></p>

```krunkscript
GAME.OVERLAY.drawText(
    txt, # str text value
    x, # num x position on canvas
    y, # num y position on canvas
    r, # num rotation (degrees)
    s, # num font size
    algn, # str alignment ("left", "center", "right")
    color, # str color
    opac # num opacity
);

# get canvas text width
num textWidth = GAME.OVERLAY.measureText(
    24, # num fontsize
    "Testing" # string text
);
```

<br><br/>

