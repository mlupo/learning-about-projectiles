# Throw_a_projectile

## Introduction @unplugged

``||sprites:Projectiles||`` are special ``||sprites:Sprites||`` that are made to move across the screen.

This allows you to easily create things like asteroids that move across the screen, or lasers that are fired from a spaceship.

## Step 1  @fullscreen

Find ``||variables:set mySprite to||`` in ``||sprites:Sprites||``, and drag it into the ``||loops:on start||``. Open the image editor for ``||variables:mySprite||``, and select or create a character.
**Just like last week make sure you re-name the ``||variables:mySprite||`` variable**

```blocks
let george = sprites.create(img`
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . f f f f . . . . . . . . . .
. . . . . . . . f f 1 1 1 1 f f . . . . . . . .
. . . . . . . f b 1 1 1 1 1 1 b f . . . . . . .
. . . . . f f f c 1 1 1 1 1 1 1 f . . . . . . .
. . . f c 1 1 1 c d 1 1 1 1 1 1 1 f . . . . . .
. . . f 1 b 1 b 1 b 1 1 1 1 d d d f . . . . . .
. . . f b f b f f c f 1 1 f c d d f . . . . . .
. . . . . . f c f 1 1 1 1 1 1 b b f . . . . . .
. . . . . . . c c b d b 1 b 1 f c f . . . . . .
. . . . . . . f f f b f b f d f f . . . . . . .
. . . . . . . . f f f f f f f f . . . . . . . .
. . . . . . . . f f f f f f f f f f f . . . . .
. . . . . . . . . f f f f f c 1 1 1 c f . . . .
. . . . . . . . . f f f f f 1 b 1 b 1 f . . . .
. . . . . . . . . . f f f f b f b f b f . . . .
. . . . . . . . . . . f f f f . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
`, SpriteKind.Player)
```

## Step 2 @fullscreen

Find ``||sprites:projectile from mySprite||`` in ``||sprites:Sprites||``, and drag it into the bottom of ``||loops:on start||``.

This will create a ``||sprites:Sprite||`` that starts in the same location as your character, no matter where it is on the screen.

```blocks
let george = sprites.create(img`
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . f f f f . . . . . . . . . .
. . . . . . . . f f 1 1 1 1 f f . . . . . . . .
. . . . . . . f b 1 1 1 1 1 1 b f . . . . . . .
. . . . . f f f c 1 1 1 1 1 1 1 f . . . . . . .
. . . f c 1 1 1 c d 1 1 1 1 1 1 1 f . . . . . .
. . . f 1 b 1 b 1 b 1 1 1 1 d d d f . . . . . .
. . . f b f b f f c f 1 1 f c d d f . . . . . .
. . . . . . f c f 1 1 1 1 1 1 b b f . . . . . .
. . . . . . . c c b d b 1 b 1 f c f . . . . . .
. . . . . . . f f f b f b f d f f . . . . . . .
. . . . . . . . f f f f f f f f . . . . . . . .
. . . . . . . . f f f f f f f f f f f . . . . .
. . . . . . . . . f f f f f c 1 1 1 c f . . . .
. . . . . . . . . f f f f f 1 b 1 b 1 f . . . .
. . . . . . . . . . f f f f b f b f b f . . . .
. . . . . . . . . . . f f f f . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
`, SpriteKind.Player)
let projectile = sprites.createProjectileFromSprite(img`
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
`, george, 50, 100)
```

## Step 3 @fullscreen

Open the image editor for ``||variables:projectile||``, and **draw** an image of something to throw.

```blocks
let george = sprites.create(img`
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . f f f f . . . . . . . . . .
. . . . . . . . f f 1 1 1 1 f f . . . . . . . .
. . . . . . . f b 1 1 1 1 1 1 b f . . . . . . .
. . . . . f f f c 1 1 1 1 1 1 1 f . . . . . . .
. . . f c 1 1 1 c d 1 1 1 1 1 1 1 f . . . . . .
. . . f 1 b 1 b 1 b 1 1 1 1 d d d f . . . . . .
. . . f b f b f f c f 1 1 f c d d f . . . . . .
. . . . . . f c f 1 1 1 1 1 1 b b f . . . . . .
. . . . . . . c c b d b 1 b 1 f c f . . . . . .
. . . . . . . f f f b f b f d f f . . . . . . .
. . . . . . . . f f f f f f f f . . . . . . . .
. . . . . . . . f f f f f f f f f f f . . . . .
. . . . . . . . . f f f f f c 1 1 1 c f . . . .
. . . . . . . . . f f f f f 1 b 1 b 1 f . . . .
. . . . . . . . . . f f f f b f b f b f . . . .
. . . . . . . . . . . f f f f . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
`, SpriteKind.Player)
let projectile = sprites.createProjectileFromSprite(img`
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . c c c . . . . . . 
    . . . . . . a b a a . . . . . . 
    . . . . . c b a f c a c . . . . 
    . . . . c b b b f f a c c . . . 
    . . . . b b f a b b a a c . . . 
    . . . . c b f f b a f c a . . . 
    . . . . . c a a c b b a . . . . 
    . . . . . . c c c c . . . . . . 
    . . . . . . . c . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . .
`, george, 50, 100)
```

## Step 4 @fullscreen

In ``||sprites:projectile||``, change ``||sprites:vy||`` from 100 to -15, so that it moves **upwards** instead of **downwards**.

```blocks
let george = sprites.create(img`
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . f f f f . . . . . . . . . .
. . . . . . . . f f 1 1 1 1 f f . . . . . . . .
. . . . . . . f b 1 1 1 1 1 1 b f . . . . . . .
. . . . . f f f c 1 1 1 1 1 1 1 f . . . . . . .
. . . f c 1 1 1 c d 1 1 1 1 1 1 1 f . . . . . .
. . . f 1 b 1 b 1 b 1 1 1 1 d d d f . . . . . .
. . . f b f b f f c f 1 1 f c d d f . . . . . .
. . . . . . f c f 1 1 1 1 1 1 b b f . . . . . .
. . . . . . . c c b d b 1 b 1 f c f . . . . . .
. . . . . . . f f f b f b f d f f . . . . . . .
. . . . . . . . f f f f f f f f . . . . . . . .
. . . . . . . . f f f f f f f f f f f . . . . .
. . . . . . . . . f f f f f c 1 1 1 c f . . . .
. . . . . . . . . f f f f f 1 b 1 b 1 f . . . .
. . . . . . . . . . f f f f b f b f b f . . . .
. . . . . . . . . . . f f f f . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
`, SpriteKind.Player)
let projectile = sprites.createProjectileFromSprite(img`
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . c c c . . . . . . 
    . . . . . . a b a a . . . . . . 
    . . . . . c b a f c a c . . . . 
    . . . . c b b b f f a c c . . . 
    . . . . b b f a b b a a c . . . 
    . . . . c b f f b a f c a . . . 
    . . . . . c a a c b b a . . . . 
    . . . . . . c c c c . . . . . . 
    . . . . . . . c . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . .
`, george, 50, -15)
```

## Step 5 @fullscreen

Find ``||controller:on A button pressed||`` in ``||controller:Controller||``, and drag it into the workspace. Drag ``||variables:set projectile to||`` from ``||loops:on start||`` into ``||controller:on A button pressed||``.

This will create an event that occurs whenever the person playing the game presses the ``||controller:A||`` button. Whenever that event occurs, your character will 'throw' a new projectile up and to the right.

```blocks
let george = sprites.create(img`
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . f f f f . . . . . . . . . .
. . . . . . . . f f 1 1 1 1 f f . . . . . . . .
. . . . . . . f b 1 1 1 1 1 1 b f . . . . . . .
. . . . . f f f c 1 1 1 1 1 1 1 f . . . . . . .
. . . f c 1 1 1 c d 1 1 1 1 1 1 1 f . . . . . .
. . . f 1 b 1 b 1 b 1 1 1 1 d d d f . . . . . .
. . . f b f b f f c f 1 1 f c d d f . . . . . .
. . . . . . f c f 1 1 1 1 1 1 b b f . . . . . .
. . . . . . . c c b d b 1 b 1 f c f . . . . . .
. . . . . . . f f f b f b f d f f . . . . . . .
. . . . . . . . f f f f f f f f . . . . . . . .
. . . . . . . . f f f f f f f f f f f . . . . .
. . . . . . . . . f f f f f c 1 1 1 c f . . . .
. . . . . . . . . f f f f f 1 b 1 b 1 f . . . .
. . . . . . . . . . f f f f b f b f b f . . . .
. . . . . . . . . . . f f f f . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . . . . . . . . . .
`, SpriteKind.Player)
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    let projectile = sprites.createProjectileFromSprite(img`
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . c c c . . . . . . 
    . . . . . . a b a a . . . . . . 
    . . . . . c b a f c a c . . . . 
    . . . . c b b b f f a c c . . . 
    . . . . b b f a b b a a c . . . 
    . . . . c b f f b a f c a . . . 
    . . . . . c a a c b b a . . . . 
    . . . . . . c c c c . . . . . . 
    . . . . . . . c . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . .
    `, george, 50, -15);
})
```

## Complete

Congratulation, your character will now throw things!

You can add ``||controller:move mySprite with buttons||`` to the ``||loops:on start||``, to make it so the skeleton can move around the screen and throw bones from different spaces.
