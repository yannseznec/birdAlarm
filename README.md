# birdAlarm
an alarm clock with destructive ideas

Made in Pd (Pure Data): https://puredata.info

This code is designed to run on a Bela microcontroller: https://bela.io 
The main patch is _main.pd

This patch is designed as an experimental alarm clock. Each time the alarm is triggered, a sound is played back and looped. On each loop, the sound is slightly destroyed. This desctruction is permanent. 

So the next time the alarm is triggered, the sound is slightly destroyed. This happens each time the sound is played. Eventually the original sound is not recognizable, and in the long run the sound disappears completely.

The initial sound is a short loop of a critically endagered bird - a Piping Plover. The sound is from here: https://search.macaulaylibrary.org/catalog?taxonCode=pipplo&mediaType=audio

The sound destruction is achieved through glitching the wavetables that are playing back the sound, and overwriting the audio array with the resulting sound. This creates a sort of compounded glitching. 

If you wish to change the sound you can modify the ys.soundSaver.pd patch.

You can also reset the sound to the original state in ys.memory_loss_demo.pd. You can not reset the sound from the patch when it is loaded on the Bela.

To make the physical build I bought a quartz battery powered alarm clock and found the wires inside that triggered the sound. I cut those wires and routed them to a digital pin on the Bela instead.

I am using one of the larger Belas, because they have built-in speaker outputs. In the current build the speaker output is connected to a surface transducer, so the whole box vibrates with the sound.

Let me know if you have any questions: yann@yannseznec.com
