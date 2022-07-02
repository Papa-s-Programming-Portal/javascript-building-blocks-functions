# javascript-building-blocks-functions

You should begin by reading three Mozilla pages: 
* [Functions — reusable blocks of code](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Functions), 
* [Build your own function](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Build_your_own_function), and 
* [Function return values](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Return_values) 

Then you should be ready to tackle the [*Test your skills*](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Test_your_skills:_Functions) for functions! But see the notes below for some advice.

As always, submit your work (for review or help) by committing your code here at GitHub.

## Notes

### Task 1

The idea is to not only write a function named `chooseName` but also to then call the function. Also, you are allowed to copy-and-paste functions from the readings. I copied the `random(number)` function, for instance, and called this function from the body of my `chooseName` implementation.  The `random(number)` function returns a random integer from 0 up to but not including `number`.

### Task 2

The canvas coordinate system is a little bit different from what you're taught in algebra.  (0,0) is the *upper* left corner of the canvas, and positive heights go _down_, not up.  Also, although the task does not make this clear, the given `x` and `y` are supposed to be the coordinates of the *upper-left corner* of the rectangle. It's also not stated that your function should have five parameters representing `x`, `y`, `color`, `width`, and `height`.  You do not have to use these variable names as the names of your function's parameters, but that would probably be simplest. You'll also need to call the function with these five parameters; in the call, you **do** need to use the names `x`, `y`, and so on (do you see why the names are fixed in the call but not in the function definition?).

The `canvas` and `ctx` variables should not be passed as parameters. Instead, your function should access these as global variables.

We saw how to clear the canvas in the loops material using a call to `ctx.clearRect`.  You will want to begin by clearing the canvas in your function as well, but the last two parameters will need to be changed since there are no global `WIDTH` and `HEIGHT` variables (hint: `canvas` is global). We also saw how to set the color of the "fill" of a closed area by assigning to  `ctx.fillStyle`. Your code can use a similar approach to set the fill color of your rectangle, except that your code will assign your 'color' parameter (whatever you name it) to `fillStyle` rather than assigning an "rgb" string as was shown in the example. Finally, to draw a rectangle is similar to clearing the canvas except that you call `ctx.fillRect` insteac of `ctx.clearRect`.  You will still pass four parameters: the upper left corner of the rectangle (two parameters, an x- and a y-coordinate), the width of the rectangle, and the height (which will represent a downward direction).

### Task 3

If your `random` function has two parameters named `min` and `max`, then here is the code you'll need for computing a random number:
```
  // Generate a random integer from min up to but not including max
  const num = Math.floor(Math.random() * (max - min)) + min;
```

Notice that your `chooseName` function should no longer store the random number directly in `para`. Instead, it should return the random number, and the code that calls your function should store the returned value in `para`.

### Task 4

I think that for once this task needs no explanation!

