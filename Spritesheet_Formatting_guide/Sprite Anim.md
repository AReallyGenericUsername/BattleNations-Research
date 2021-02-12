# How to format animations to work with unity.

This guide will show you how to process spritesheets extracted from the Patreon BN build to make them work nicely with unity.
When importing spritesheets from the Patreon Build, one may notice that the conventional slice method does not quite work well because of the uneven dimensions of the spritesheet. Because of this, processing is required to format the sprites correctly when animating and slicing in unity.

## Getting the proper dimensions

Unity's sprite editor really sucks when processing dimensions and such which is why I use something else to get the proper dimmensions.

![Behold, the spritesheet animator](https://github.com/Agenericusername5973/Testing/blob/main/Spritesheet_Formatting_guide/SSA.PNG)

You can find the Spritesheet editor by googling it because I am too lazy to include the link.

Regardless, when you play the spritesheet editor your animation should look like complete and utter garbage and that is ok. To fix this you just need to play with the image dimensions until the image stops drifting. Another thing that you should do is increase the frame count to ensure that the animation does not get cut off somewhere. ***Please*** note that Unity does not accept negative offets, so find another way if you are using them.

After doing this your animation should look smooth and ready. 

![now it looks good.](https://github.com/Agenericusername5973/Testing/blob/main/Spritesheet_Formatting_guide/SSA2.PNG)

From here take note of the sprite height, width, padding and other things that you messed with.

## Finding what to add

After doing this, open up unity and import the spritesheet. After doing this open up the sprite editor and copy the dimensions and offsets in and slice via cell size. Unless you are ***really*** lucky your spritesheet should look a bit like this

![...](https://github.com/Agenericusername5973/Testing/blob/main/Spritesheet_Formatting_guide/SSA3.PNG)

What we basically have to do now is resize the image based off of the next needed dimensions. So what we do is go to one of the unsliced frames and see what it needs to get to the target dimension.

![These dimensions are not right.](https://github.com/Agenericusername5973/Testing/blob/main/Spritesheet_Formatting_guide/SSa4.PNG)

Our target dimensions gadthered from the Spritesheet Animator was 166*139 meaning our frame is 10 pixels off. With this knowledge it is off to GIMP.

## Adding what we need

While you do not necessarily need GIMP, I use it because it is a good and free alternative to photoshop. Any image manipulation software should do. Once you have opened up the spritesheet in GIMP just resize the canvas by the amount required to slice the frame. In our case we need to add 10 pixels to the bottom. 

![dimensions set](https://github.com/Agenericusername5973/Testing/blob/main/Spritesheet_Formatting_guide/SSA5.PNG)

now export that sucker ***without compression!!!***

## Finishing up

If we import our modified spritesheet into unity and splice it, we should have a full colum or row. Repeat these steps for the row/colum on the other side.

![dimensions set](https://github.com/Agenericusername5973/Testing/blob/main/Spritesheet_Formatting_guide/SSA6.PNG)

And just like that we have an animation that works!

If you don't know how to code or anything like that and you want to help then please do help process the animations to make them smooth!

*Thanks for listening to my ted talk*


