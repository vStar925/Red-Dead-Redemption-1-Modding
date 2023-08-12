NOTE: This guide only covers the Xbox 360 version of the game.

NOTE2: A recent update to MagicRDR allows directly editing texture dictionaries. AKA you no longer need to use RAGE Console Texture Editor. I will update the guide in the future.

# Installing & Creating Mods
I. Everything You'll Need
------------------
* An .iso of either Red Dead Redemption, Undead Nightmare, or RDR: GOTY (GOTY will be used in this guide)

* [Red Dead Redemption 1 Modding Tools](https://archive.org/details/red-dead-redemption-modding-tools.-7z)

* Photoshop, Paint.net, GIMP (if you're editing texture files. Not needed if you're just installing mods or modifying xml/xtbl files)
	

II. Extracting the ISO
--------------------
You'll first need to extract the raw contents of the Red Dead Redemption .iso file if you haven't already.

1. Run wx360 and navigate to the Red Dead Redemption .iso. (If you downloaded the Modding Tools, this program is located at `Tools/Xbox 360 Tools/wx360`

![](https://i2.lensdump.com/i/1QT38r.png)

2. The file structure will look like this. Press the extract all files button. I like to keep them in my games folder right next to the original .iso, but it doesn't matter where you put it.

![](https://i2.lensdump.com/i/RODm6r.png)

III. Exploring .RPF archives
-------------------------------------------------------------
1. Open `MagicRDR.exe`

2. Click `File>Open` and navigate to either `rdr2_layer0.rpf` or `rdr2_layer1.rpf`, wherever you extracted them to. (This guide will be using the former for example's sake)

3. Navigate to a file you want to edit. Since the guide primarily focuses on texture edits, you'll be looking for .xsf or .xtd files. (This guide will be using `popup.xsf` but the process is the same for .xtd. (NOTE: MagicRDR cannot open .xsf files directly, but it can open .xtd's. It cannot, however, import into a .xtd (This is where the next tool comes into play.)

Note: All of Rockstar's RAGE engine games use texture dictionaries to store a majority of textures. Think of a texture dictionary as an archive that holds .dds images. You're not editing the .xtd or .xsf *directly* but the images stored *inside* of them.

4. The process will be the same for either file extension, so extract either .xsf or .xtd anywhere on your computer by right-clicking and selecting `Extract File`.

![](https://i3.lensdump.com/i/RONlFv.png)
	
IV. Extracting Textures from a Texture Dictionary
---
1. Inside RDR1 Modding Tools, navigate to `PS3-Xbox360-RAGE_Texture_Editing\Console_Texture_Editor\RAGE_Console_Texture_Editor-v1.5` and run `RAGE Console Texture Editor 1.5.exe`

Note: For me at least, this program is pretty buggy but it's the only one I've found that does what I need it do. Basically no matter what you do, it will throw an error. Just hit continue until the errors are gone.

2. Open your extracted .xtd or .xsf file. Go to `Functions>Export All` and export all the images to a new folder.

3. Depending on which file you are modifiying, you may get anywhere from 1-100+ .dds files in this folder. Find the texture you want to edit here and note the name. Now go back to `RAGE Console Texture Editor`, find that same filename, and note the texture format as noted at the bottom of the program. Now open the texture in  *PhotoShop, Gimp, Paint.net, etc.*


V. Editing a .dds file and re-importing it into a texture dictionary
----------------------

1. After importing the texture, make whichever edits you please & export the file as a .dds texture (with the same name), changing the compression according to the attached image below.

![](https://i1.lensdump.com/i/ROfuf0.png) [Source](https://www.se7ensins.com/forums/threads/gta-v-gta-iv-rdr-texture-modding-tutorial-for-ps3-xbox-360.1835853/)

2. Return to `RAGE Console Texture Editor` and find the name of the texture file you just edited. Highlight it and select `Import` in the bottom left. Find your recently edited texture and import it.

3. Save the file and exit this program.

VI. Final Steps
---

You should now have an texture dictionary with modified textures after saving it in the previous step.

1. Return to `MagicRDR`. If you didn't close it before, you'll still see the file you extracted in Section III. If not, just search for it again in the top-right corner.

2. Right click the .xsf/.xtd file, and click `Replace`, selecting the file you saved in Section V, Step 3.

3. In MagicRDR, go to *File>Save>Current*. Click yes to both prompts and wait for the process to finish. (After it tells you it's finished, it becomes unresponsive for a few seconds. Just give it a little more time and once it's responding again, close this program.

4. In Xenia, open default.xex in your extracted Red Dead Redemption folder to run the game. If it doesn't crash, congratulations, you did it. :)
	

