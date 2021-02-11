# EDCShaders
NWN Enhanced Depth and Contrast Shaders v1.2.1, for NWShader

Neverwinter Nights graphics are pretty dull and flat by today's standards. These NWShader shaders aim to enhance the contrast and depth of the image, while respecting the original mood of the game.

What does this mod do, exactly?

   > It makes would-be bright surfaces actually bright, by applying a pseudo Bloom effect that does not blur the image.
   > It enhances contrast by adjusting low color tones ("Lift", by default) and high tones (through the above, and also by color Gain).
   > It adjusts saturation intelligently to make originally "out-of-place" objects blend better with their environment.
   > It applies a pseudo SSAO (Screen Space Ambient Occlusion) effect to the image, further enhancing its contrast and depth.
   > Finally, it applies a very subtle sharpening effect to the image.

The defaults I've chosen are quite conservative (see screenshots in neverwintervault.org), but the effects can be easily configured to be more prominent if you wish. Bear in mind that a bunch of small tweaks can compound to make a big difference, and this is most noticeable while playing!

Requirements
------------
   NWShader, version Bahamut 0214. Newer versions may also work, adapting the configuration file, but this is the only one that would do so reliably for me. You can get it here: https://sourceforge.net/projects/nwshader/files/Offline%20Packages/

Installation
------------
   Copy the contents of the mod's "nwshader" folder into the game's nwshader folder, overwriting when prompted. If you installed NWShader correctly, the shaders should work right away with their default settings.

Tweaking
--------
In the "shaders" directory, open sceneAdjust.cgfx or sceneSharpen.cgfx with a text editor like Notepad++, and tweak the values of the variables at the top, staying within their respective intervals detailed above them.


Version History:
---------------
  1.0   : Initial release.
	1.1   : Distant fog is now darker (by default), and closer to vanilla. Fixed some oddities with depth calculations, occurring against sky when moving the camera. Added LumaSharpen shader!
	1.2   : Major code modifications. The quality of distant transitions into effect of Bloom and SSAO is now much better. SSAO is softer and decays in the distance, heavily reducing distant blur, blending better with fog (which helps grass immensely when against it) and eliminating some minor artifacts that used to occur with farthermost vegetation. Color and brightness functions are a bit different, you might have to readjust your settings. I reorganized settings in the files are provide more info about them. General code optimization.
	1.2.1 : Bloom is now done differently - it is better at extracting additional detail from textures, plays better with color gradients and its associated tint is more subtle (and configurable). Simplified Sharpen code (result does not change). Bundled the appropriate license files with the download.
	
	
--------------

Licenses and Credits:

All software provided in the NWN-EDCShaders package, except for the SSAO shader detailed below, is licensed under the MIT license.

All credit for the SSAO shader I've modified goes to peachykeen, the original author. This SSAO shader, contained in sceneSSAO.cgfx is licensed under the GNU General Public License v3.0.

All credit for the LumaSharpen shader I've ported goes to CeeJay.dk, the original author. This LumaSharpen shader, contained in sceneSharpen.cgfx is licensed under the MIT License.
