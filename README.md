# Reveal_Stairway_Material_and_Documents

his a NEW Repository file that comes from the original Repository 'Reveal_Stairway'. 

This will only contain my BLOG, images and photoshop doucment. 

.......................................................................

This is my independent project for the collaboration of team ‘Break the Build’.
 We have been assigned to test and produce new effects and coding so that we may join together in the future to create our survival horror game.
IN MY GITHUB REPOSITORIES, look for ‘Break-the-Bill’ as that is our collaborative repository. You will see the list that we have come up with.

My assignment from the team from the last few weeks:

1.	Create animation for platforms to appear e.g. stairs appear before the player (level Blueprint, Matinee).
2.	Operate a key mechanic, door can only be open by a key (include widget text/images to pop up).

NOTICE 22/11/2017:
I’ve forgot to add my screenshot and videos from the last few projects a while ago, so go check them my repositories BluePrintLesson1 and ThirdPersonProject for those updates. 


1: Creating animation for stairs to appear before the player

Mood board (Pinterest): https://www.pinterest.co.uk/gabrielawoch100/break-the-build/
To check out my videos: Reveal_Stairway > Video Clips

Brief summary of my progress:

![](Screenshots/Maitnee%20Graph.jpg)
![](Screenshots/Maintee%20Level%20BP%20fixed%20%2B%20Reverse.jpg)

Blue Print and Matinee display highlighting the directional path for the floorboards

Video: [1, 2 and 3]
Soon realized after a couple of days of researching that I found out that there were many ways of how to make an object move, whether by the Boolean system that effects their location, so on and so forth. But what I found that appears to me the most the simplest to construct is to use the Matinee mechanic. Allowing to animate multiple object in one program. The only problem is, is that it has to be made in Level blueprint and so I have to reconstruct from scratch if I were to use this in another project. Also need to find ways to keep my layers clean as this takes a lot of induvial object to be inserted in.  
Had a problem when I first made it was made it, the trigger box got caught up with the animation. So I can’t make a ‘Reverse’ command if I wanted to. 

Video: [4 Stairway Animation fixed]
I figured out how to stop the trigger box from animating with the Matinee. By detaching the box that was an actual a component within the first starting object. I then recreated the box as a separate actor and join it back to the blueprint. See how clean and simple the blueprint looks with matinee?

![](Screenshots/BP%20for%20Stairs%20and%20Door%20mechanic.jpg)
Blueprint for the Matinee mechanic for the Stairs and Door


2: Creating a Door mechanic that can be opened up by a key 

Plus adding text that will help the player tell what they need to do or what they got.
Took a couple of days to research whether to make the opening door mechanic work on CLASS BLUEPRINT but the tutorials that I found was not very specific and didn’t use the First-person character. The blueprint inputs are very different between first and third person characters. So it for now, to make things easier I used the matinee system again and worked my way around that.

![](Screenshots/Door%20mechanic%20changed%20so%20it%20counts%20to%20only%20pressing%20the%20E%20key.jpg)
Inserting the ‘E’ key input into Blue print within the Matinee. Making the door opening door mechanic. I added the E input in the project setting.
This was before I added the Boolean variable for the key mechanic.

![](Screenshots/1%20Key%20Blueprint%20to%20Door.jpg)
![](Screenshots/2%20Key%20Blueprint%20to%20Door.jpg)

Had to set up the Boolean variables on my first person’s blueprint and then transfer them onto the LEVEL Blue Print.
I’d used a random jar object that I have made in the past to serve as the key. I added the collision effect and had to rearranged the trigger event input just to make the whole blueprint worked. 

With that working, I need to now tell the player how to operate it. So, a text display would be simple enough. I figured out that I can use widget for this part. 
As an artist I had experience with drawing out UI on Photoshop, but never had the chance to insert some in the game. If we want to make the game stylized and not just showing plain old text on screen, drawing the menu out would be a much more effective thing to see on the screen.

![](Screenshots/UI%20Inventory.jpg)
Playing around making UI display on photoshop, I added text within the box.

To see my drawn UI: Reveal_Stairway > Screenshots > Drawn_UI

Next step was trying to learning how to insert the UI images that I made into Unreal through Widget. I didn’t use text format for this experiment, just the image format along with its fading effects. 

![](Screenshots/2%20WIDGET%20Press%20E%20on%20class%20BP%20trigger%20box.jpg)
Attempting to add the Widget into Blueprint.

The correct way to add the imaged text for telling the player to press ‘E’ when coming to the door was to separately open up the door’s trigger box on CLASS blue print and then added the widget set up there.

![](Screenshots/1%20WIDGET%20Obtain%20key.jpg)
Blueprint of attaching the “Obtain Key” widget when you touched the key. It was very tricky to figure out how to destroy the key’s trigger box as well. Because before, you could just continue to walk over that spot and the text will still reappear after you first picked up the key.

Video: [21 Key Mechanic without Locked sign].
This was the last thing I achieved without coming back for a long time. Managed to get the widget ‘Press E’ to appear but can’t figure out how to get “It’s Locked” image to appear with the condition of pressing the ‘E’ input and without the key itself.
Video: [22 ‘It’s Locked’ Issue].
After spending over 3 hours on trying to figuring how to get the text to appear on the screen, the closet bit I got to which you can see it in the video, is to use the String Print, I initially tried to make a new variable that was set up only for the ‘E’ input to be the new condition for the branch/Boolean mechanic, but that didn’t work either. Overall the main issue was to address the computer which condition I’m trying to analyze, when things do work out, it unfortunately disables the other entire system of when the player does get the key and so you can’t open the door. For now, I can only leave for now and see if my fellow team mate might help figure the problem. 
Right now, I need to start my next plan or creating some bushes and hedges for the game.

3: Merging our separate object into one Unreal Project.
PROJECT IS NOW MOVED ONTO THE GROUP UNREAL PROJECT (Our_Nightmare)
To it keep it simple, we each made our level map to install all of the new things into the same Unreal project without colliding when committing our work.
Learnt to Migrate (transfer one blueprint/ asset to another project)
Issue encounter: 

•	Only Class blueprint can be transfer over to the new project. Meaning I had to start from scratch to add in new matinee and build up the level blueprint.
•	Images had to be reinstalled into the widget. 

