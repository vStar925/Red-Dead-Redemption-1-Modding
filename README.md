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
	
IV. Extracting .peg_xbox2 files
---
1. Inside the newly created folder, find a .peg_xbox2 file you want to edit. _For the sake of this guide, I'm editing interface-backend.peg_xbox2._ Copy your file out of this folder and directly into SR1 Mod Tools.

2. Drag your .peg_xbox2 file onto PegConvert.exe. A new folder with the name of the file with the suffix __unpack_ is created. Go ahead and delete that suffix since you're going to need to do it later anyways.

Your folder should look something like this at this point.

![Your folder should look something like this by now.](https://i1.lensdump.com/i/1QEoWb.png)

3. Inside of your newly created folder, you will find a variety of .DDS files (if you don't, your .peg_xbox2 was probably empty. Try another file. interface-backend is not, for example). **_Take note of @peg.xml. You will need this file later_**

_**Also at this point, I would recommend copying interface-backend (or whatever file you just extracted) to a separate folder. We'll be editing the folder in this location so we'll still have the original backup in SR1 Mod Tools. Optional, but highly recommended so you don't have to extract everything again if something goes wrong.**_

4. Decide on a .dds file you want to edit. Open it in PhotoShop and continue onto Section V.

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

	

