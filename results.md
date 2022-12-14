## Results

### Testing
Since the LCD screen was the only peripheral device that we could perform tests on, all our tests were done using the screen. For example, to test if the joystick is working correctly, we displayed different shapes or texts on the screen depending on the joystick inputs. We also used PuTTY in the beginning, before we got the LCD screen, to test if the connections for the buttons are correct; but after we connected the LCD screen and became familiar with displaying something on it, we mainly used it to test and debug our code.

### Speed of Execution 
As explained in the Program/Hardware page, we switched our programming language from MicroPython to C in the middle of the project to fix the serious flickering issue of the LCD screen. In MicroPython, we tried using multithreading to separately execute the ball and the paddle movements, but it did not work out well and we had to stick with one entire while loop that runs the game. However, after our transition to C, we were able to use multithreading much more easily, and the execution speed was much faster - at least 10x faster than micropython. This fixed the flickering and delay issue that we had with MicroPython.

### Accuracy
We spent a lot of time debugging after implementing our logic through coding, mainly to ensure that the games do not produce any bug. Some small-scale calibration works included choosing the right speeds for the ball and the paddle in Pong, making sure that the apple is randomly regenerating in Snake, or adjusting the size and shape of the arrows and the duration of delays in Memory; larger-scale debugging included figuring out how to implement the algorithm for continuing the game or returning to the main menu.

### Safety in Design
We tested to ensure that the level of brightness of our LCD screen does not disturb the player's eye health. Although the screen became more brighter when we plugged in the battery pack instead of the USB cable that connects the RP2040 board to a laptop, we confirmed that the brightness is still within the safe level. We also made sure that none of our hardware parts has a sharp edge that can potentially result in cuts; after using a dremel to make a hole, we used a piece of sand paper to make the cut edges smooth. We also used electrical tapes and heat shrink tubes to prevent the metal part of the wires from being exposed or touching each other.

### Usability
Although Pong and Snake do not show the game rules before the games start, we believe that they are straightforward and can be understood after a few tries, even if the player has never played them before. For the Memory game, we included a screen on which the game rules are explained, as this game was designed and implemented by us, unlike the other two famous games. 
