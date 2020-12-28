**APU with patched Microcode**

I integrated the Microcode-Patch to the APU2, APU3, APU4 and APU5 to the BIOS.

The guide I used can be found [here](https://github.com/pcengines/apu2-documentation/blob/master/docs/microcode_patching.md).


The newset Bios as of writing is mainline: v4.13.0.1

I will try to update the BIOS file to the newest mainline as soon as one comes out.




**How to Flash the BIOS**

**Step 1**
Install/Download [TinyCore](https://www.pcengines.ch/tinycore.htm).

**Step 2**
Start the executable program.

Follow the industraction and make sure to tick the reformat box.

(At least for me it booted not always if I did not checked the box, tested with Windows 10.)

Then use a USB drive **!Warning!** all data will be erased.
Wait till the programe is finished.

**Step 3**
Place the APU-Bios into the root directory.
Boot the USB drive from the APU and do:
>flashrom -w "APU*-BIOS.rom" -p internal 

*APU from 2-5

It will flash the BIOS this may take a few minutes.
When it's finished do a colboot and you're good to go.
