# WordStream: a high performance reading app

WordStream displays text to be read in a consistent place on the screen, so your eyes don't have to move.

This project was written to experiment with various frame rates and formats to try to provide improved reading experiences.

WordStream allows you to display text on the screen very rapidly. This allows higher speed reading,
as well as testing of reader capabilities.

You can try this project on its [github page](https://cocode.github.io/word-stream/)


# Settings

WordStream allows users to select intervals (ms) , and length of text to be displayed in each frame,
and displays some statistics about this.

## Min interval (ms)
Sets the minimum frequency that you want the text to be displayed for. If you pick 100ms, the text will be displayed eveery 100ms, or ten times a second.
The text may be displayed for more time that this, based on your display characterists, but it won't be less.

## Max characters
This is the maximum number of characters to display at one time. This is a soft limit, as it does not break words in half. So, if you had the limit set to eight,
the following would still show all of the second word.

```
hello, madagascar
```
## Snap to display


# Statistics

## Display
How faster your display is updated. We can't update any faster than that, nor can we change that rate. 

You'll see two numers, perhaps
```
 	120.00 Hz 	8.33 ms
```
the 120 is the number of times per second your display is updated. The second is, given that frequency, how long does each refresh take. 


## Target

The 'target' is the best we can do, given your display. If you ask for an interval of 7, we will have a target of 8.333, since that's as close as 
your display will let us get to 7ms. So, anything less that 8.3333 goes to 8.3333. Anything between 8.3333 and 16.6666 will go to 16.666 (which is 60 times a second), etc.


## Actual 	59.97 fps 	16.68 ms
This is the speed we are actually getting. If your machine is busy, we may not be able to keep up with the goal. Otherwise it should be very close to the target.

## Avg
Is the average time we are taking between updates.

## Frames
Frames is the total number of frames displayed so far.
