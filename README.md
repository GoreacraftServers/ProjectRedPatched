Blah blah blah actual mod description below, no one cares.
It's yo boi, music, here to tell you how to properly build this gay project.

If you are using intellij, congrats, you're doing great. You need to import the project as a gradle project,
there should be a dialogue box at the bottom asking you, just click it and auto import. This will not appear if you've 
use gradle in the past. Intellij gets salty that this project is using 
gradle version 2.6, and claims that it isn't compatible. That is wrong. If you clicked that shiny
blue link to upgrade gradle to version 4.x.x, you're dumb and need to try this again. You actually don't even
need to touch gradle. Now comes the moderately hard step. There is a directory called lib, and in it is cofhcore.....
Right click on it, then towards the bottom, there is an option that says Add as Library...
Click ok on the dialogue box. With that, the hard stuff is all over dumb dumb. Remember, use intellij.
Open up build.gradle located on the top, and scroll down until you get to line 207.
If you are using the superior ide, there will be a green play button next to it. Click it and then select the top option.
Tbh at this point it might give you errors, but like... those are practically warnings, don't worry about it, let the build finish until you have the output in /build/libs.

Back to your regular scheduled README!






ProjectRed
==========
Project Red is a mod written for Forge Multipart. It brings vastly improved redstone control to Minecraft via compact wiring and integrated logic gates.
- [![Build Status](https://travis-ci.org/MrTJP/ProjectRed.png?branch=master)](https://travis-ci.org/MrTJP/ProjectRed)
- [Minecraft Forum Thread](http://www.minecraftforum.net/topic/1885652-)
- [Website](http://projectredwiki.com)



CB’s policy for requesting new gates:
-------------------------------------

For anyone wanting a new logic gate. Here's my proposal.

1. It needs to have a purpose. You will need to provide examples of where this gate will be useful.
2. It needs to be something that cannot be constructed in 3 existing gates or less.
3. You must completely describe how it will function.

As an example, here's the RS latch.
The gate has inputs on the left and right, outputs on the top and bottom.
When you activate the left or right input, it switches into that state. When in the right state, the top output is on, when in the left state, the bottom output is on. It will also output from the input sides based on state.
If both inputs are turned on, the gate should deactivate until they are both turned off. If both sides are turned off at the exact same time, it will pick a random state.
It can be flipped with the screwdriver.
It also has a second screwdriver mode where the inputs do not get powered based on state.

While the RS latch could technically be made with 2 NOT/NOR gates, it is a very fundamental logic circuit. Additionally, having only a two tick delay, instead of a 4 tick is quite useful.


Should you be able to describe your proposed gate in this format, create a feature request on the GitHub repo for ProjectRed. MrTJP and I will be notified and will be able to provide you feedback on your proposal.



Developing:
----------
Setup is slightly different depending on what system and IDE you use.
This assumes you know how to run gradle commands on your system.
The base command, `./gradlew` being used below is for Linux or Unix based systems. For windows, this would simply change to `gradlew`.
Of course, if you dont need to use the wrapper (as in, you have gradle installed on your system), you can simply go right to `gradle`.


1. Clone repository to empty folder.
2. Cd to the repository (folder where `src` and `resources` are located).
3. Run `./gradlew setupDecompWorkspace` to set up an environment.
4. Run `./gradlew eclipse` or `./gradlew idea` appropriately.
5. Open your IDE using the generated files (i.e., for IDEA, a ProjectRed.ipr is generated in `./`)
6. Edit, run, and debug your new code.
7. Once its bug free and working, you may submit it as a PR to the main repo.