

# Steady Particle Generator for Quill

**OVERVIEW**

This is a mini-tool to test out automating simple particle effects for Quill. Putting it out there in case it’s useful as is, but also in case it inspires other ideas/further development. It’s based on Goro’s tutorial, the Steady Particles section (around 6:56): 

The idea: you draw one single particle drawing (e.g., one sphere) in Quill, and then using this tool, tweak all the other settings to create a steady particle effect like Goro demonstrates in his tutorial. In practice, it may not save that much time, especially for those who are quite familiar with the practice of creating steady particles effects. But it may be helpful to or fun for some users as is, and/or could spark other ideas for future development.

**HOW TO USE:**



1. <span style="text-decoration:underline;">Select Quill project folder (button)</span>. This should be the top level folder (contains Quill.json, State.json and Quill.qbin) of the Quill project in which you’ve already drawn the original starting particle. 
2. <span style="text-decoration:underline;">Select the layer</span> containing the starting particle from the dropdown. The idea is that you are just creating a single particle (a square or cube, etc). It should be a static paint layer. If it’s a layer containing frame by frame animation, only the first frame will be considered.
3. <span style="text-decoration:underline;">Set the scale</span>, which uses the 20X20 Quill grid as the default face for a cubic area. That is, a 20X20X20 cubic area that sits atop the Quill grid. Users can adjust the X, Y and Z scales to create different sized particle array areas.
4. <span style="text-decoration:underline;">Duplicate and randomly reposition and rotate particles</span>. 
    1. First, select how many duplicates of the original particle drawing/object you want in the array space you’ve selected above.
    2. Keep the rotation checkbox checked to randomly rotate objects. Uncheck if you want all objects to maintain the original orientation and only change the position.
5. <span style="text-decoration:underline;">Animation</span> 
    3. Select the number of particle offsets for the effect. The array of particles you created above will be duplicated over this many times.
    4. Choose the time in seconds at which you want the animation loop to occur.
6. _OTHER USES_
    5. To automate a moving background effect, set the number of drawing duplicates to 0, and choose your values for the animation/offset dropdowns.
    6. For creating a randomized particle array only (no animation), just set the number of particle offsets to 0.
    7. For populating environments with trees, buildings,, edit the scale so that the grid size works for your task. For example, set the Y scale to the height of your object to ensure that they stay “grounded.” (If your object is about 5 Quill squares high, then this would be 0.25, as it’s done as a scale of the grid length/height, which is 20X20). 

**IDEAS FOR TWEAKS & FUTURE DEVELOPMENT:**



* Change the XYZ scale options to values that are more intuitive if thinking in terms of a scale of the Quill grid doesn’t feel natural. Other options, like value ranges for the numeric dropdowns, could also be changed to values that might be more useful to users.
* Allow users to limit random generation across a plane directly instead of using a 3D space. For example, this could be useful for populating objects on a flat ground.
* Create more options for rotations that can limit rotation by axis (e.g., only rotate around the Y axis). 
* Allow users to customize the particle array area by providing a cube paint layer from Quill.
* Make tweaks to allow this tool to work directly for rain/snow effects in the style of Goro’s tutorial.
* Allow for randomization of scale and proportion for the original object.
* Explore options for other particle effects and more complex animations.

**IDEA & DEV CONTRIBUTORS & NOTES**

Joan Charmant created the C#/.NET library called SharpQuill: 

[SharpQuill is an open source .NET library for reading and writing Oculus Quill scenes.](https://github.com/JoanCharmant/SharpQuill)

This steady particles tool heavily relied on SharpQuill to read, modify and write Quill projects. Thank you, Joan, for making this library free and available!

Nick Diaz came up with the idea to explore ways to automate aspects of VFX creation for Quill after collaborating with **Jari **on a text generating tool for Quill. 

Anna Kasunic worked on the code for this project. 

**HAVE IDEAS, QUESTIONS, BUGS?**



* Add comments directly to this doc. 
* Join the [Virtual Animation discord](https://discord.gg/virtual-animation-696504903060947116)! Reach out to Anna and others on discord. Can also email Anna, same name as on discord (amkasunic) AT gmail.
* Feel free to fork or get ideas and dev directly! 
