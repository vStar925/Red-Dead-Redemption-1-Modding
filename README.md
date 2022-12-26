NOTE: This guide only covers the Xbox 360 version of the game.

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
	
IV. Extracting & Importing Textures in a Texture Dictionary
---
1. Inside RDR1 Modding Tools, navigate to `PS3-Xbox360-RAGE_Texture_Editing\Console_Texture_Editor\RAGE_Console_Texture_Editor-v1.5` and run `RAGE Console Texture Editor 1.5.exe`

Note: For me at least, this program is pretty buggy but it's the only one I've found that does what I need it do. Basically no matter what you do, it will throw an error. Just hit continue until the errors are gone.

2. Open your extracted .xtd or .xsf file. Go to `Functions>Export All` and export all the images to a new folder.

3. Depending on which file you are modifiying, you may get anywhere from 1-100+ .dds files in this folder. Find the texture you want to edit here and note the name. Now go back to `RAGE Console Texture Editor`, find that same filename, and note the texture format as noted at the bottom of the program. Now open the texture in  *PhotoShop, Gimp, Paint.net, etc.*


V. Editing and saving a .dds file
----------------------
_**NOTE: Even if you're familiar with Photshop, please don't skip this section. There is a very specific way you need to save the files that if you fail to do, the game either won't load or the textures will be corrupt.**_

1. For the sake of this guide, I will be editing _hud_sheet_08.dds_.

2. Make whatever edits you please. 

![](https://i2.lensdump.com/i/1QEu97.png)

3. The next step is the reason I made to sure to mention not skimming over this section. Before you save your edited .dds file, open _@peg.xml_ in your mod folder if you created after Step 3 in Section IV. If not, just wherever your .dds file is located.

4. Find your texture file name in this file.

![](https://i3.lensdump.com/i/1QEDLr.png)

5. Take note of the format of the texture and whether or not it has the flag "HasAlpha". Hud_sheet_08.dds is DXT3 and HasAlpha, for example.

6. Return to Photoshop. Go to File>Save As and save as Intel Texture Works (.DDS), overwriting your original file.

7. You will see this window. If your texture is DXT3 and HasAlpha, save it with the settings below.

![](https://i.lensdump.com/i/1QENGF.png)

If your texture is DXT1 and had "None" under flags in @peg.xml, save it with these settings.

![](https://lensdump.com/i/1QEfk3)

8. If your texture was DXT1 and you saved it as such, you can skip this step. If your texture was DXT3, continue to step 9.

9. After format, change the value from DXT3 to DXT5. Save the file.

![](https://i2.lensdump.com/i/1QEFl0.png)

VI. Repacking your files and final touches
---

_Don't worry, texture editing is the hardest part of this guide. From now on, everything is as simple as can be._

1. Drag the interface-backend (or whichever folder you extracted) folder onto _PegConvert.exe_ inside of SR1 Mod Tools. A new .peg_xbox2 file appears in your mod folder with the suffix _pack.

![](https://i2.lensdump.com/i/1QEwNM.png)

2. Delete the _pack suffix.

3. Drag your newly created .peg_xbox2 file with the suffix deleted into the _pegfiles folder_ inside SR1 Mod Tools.

4. Run pack_pegfiles.bat (edit it using the image in Section III, Step 3b if you're packing a different folder.) A new pegfiles.vpp_xbox2 appears in SR1 Mod Tools. Drag this file in your packfiles folder inside your extracted Saints Row folder. Replace.

YOU'RE ALL DONE! Go in game and test out your mod :)

![](https://i3.lensdump.com/i/1QEyiQ.png)

	

