# What is a lightwarp and how can I create my own?
This is a simple guide on how to edit a Team Fortress 2 lightwarp


The Source Engine's lightwarp technique is utilized to add a sort of glammoring effect on an entity. Team Fortress 2 utilizes this technique to be able to apply a cell-shaded effect to suit it's cartoony art style.  

![image1](https://github.com/user-attachments/assets/67dfa86e-6cdf-45af-943f-dd4791d6c165)
Example of Team Fortress 2's artstyle and lightwarp application ingame
Notice how characters who are not directly in the bright sunlight do not "glow", while the ones that are do indeed glow. More to be elaborated.
 <br>
 <br> 

![image2](https://github.com/user-attachments/assets/0b2cbcd8-67cd-45ed-a657-4014a0e89af0)
 <br>
 (Image taken from Valve Developer Community, https://developer.valvesoftware.com/wiki/$lightwarptexture)
 <br>
Heavy character without his standard textures.
On the right, you can see the lightwarp cell-shaded effect being applied to the model.
<br>
<br>
<br>
Now we question, how does a lightwarp work? and why do we want to change it?
<br>
The lightwarp wraps around an entity and brightens its texture depending on what amount of light the entity is currently standing on.
The object’s actual color remains unaffected. Look at it like an object behind a stained glass. From the view of the stained glass, the object has a colored tint depending on the glass’ color. Nevertheless, the object remains the same original color behind it, and only when viewed from the stained glass, does it carry this colored tint.
<br>
However, what exactly is what gives it the specific color that is reflected when the light shines on it? Simple! It’s just a texture in the VTF format (Valve Texture Format).
<br>
<br>
A VTF file is essentially a texture format used by the Source Engine and they are usually called by a material file (which contains info on how the engine decides what textures to draw, how to draw them, how to treat said textures after being drawn, and how they react). 
![image](https://github.com/user-attachments/assets/c8917058-eef1-4f60-8e81-0068e809d51e)
<br>
Example of a VTF file and it's properties once opened in an editor.
<br>

<br>
In TF2, a multitude of entities and models have a lightmap applied to them to achieve the desired cell-shaded effect. Thus, a model will have a specific lightwarp tied to them, and with multiple models, that means there are a multitude of lightwarp files. If one would want to modify these lightwarp textures, we would first have to find a way to open VTF files, and a way to edit them as well, while also having them be compiled and applied to the game itself.
<br>
<br>
To do so, we have a couple of options. We could download the VTF file viewer called "VTFEdit" (used in the example above), however this application is mostly used to modify different texture properties and not much edit an actual texture. I personally went ahead and downloaded a plugin for PAINT.NET, which is a sidegrade to Microsoft's paint application that is default to Windows operating systems. The application contains a multitude of tools that far surpass Microsoft's version and then goes ahead and has even more capabilities than it as well. This can be downloaded here (it's free): https://www.getpaint.net/download.html
<br>
<br>
The plugin I went ahead and got was Nem Tool's PAINT.NET VTF plugin. The website has apparently been down for a while, however, thanks to the web archive, we can go back and download it. It can be found in the following link: https://web.archive.org/web/20200201044118/http://nemesis.thewavelength.net/index.php?p=50
<br>
<br>
Once that is done, we can go ahead and get right into modifying a lightwarp. For the sake of your sanity, download my modification of the lightwarp so you can have all the files needed to make your modification. I'll still go ahead and show you the process and results here.
<br>
<br>
The following is an image of one of the lightwarp files. 
<br>

![image](https://github.com/user-attachments/assets/c96c30d4-e822-49a8-a21a-0a4c4d219d5b)
<br>
I decided to make my lightwarp the color green, do not laugh! (it has a certain charm to it!)
<br>
<br>
You will quickly notice that a lot of the files share the same lightwarp texture, by that I mean that while there are different files for multiple entities, the texture still remains the same (there are some exceptions, but in total there are 2 unique textures among all the files). The process of actually going ahead and painting the lightwarp is up to the most passionate of graphic designers (not me), thus you should have a smoother experience when editing the files. Note that for the texture shown above, it is recomended that you start with a darker texture on the left and then gradually proceed onto a lighter texter until you reach the other end. I went ahead and did a little exotic texture here, and trust me, it does not look as spectacular as I thought it would ingame.
<br>
<br>
Now you have edited the lightwarp textures, how does one implement it onto the game? It's pretty simple thanks to another tool created by "cukei" and his team over on GameBanana (https://gamebanana.com/tools/19049). Due to TF2's online ecosystem, some modifications dont usually show up on officially hosted servers, this tool allows that and also simplifies the way to install lightwarps.

![image](https://github.com/user-attachments/assets/39ed72cf-97a8-4e4b-b03b-9c6dc006a55f)

<br>
Follow the instalation guide and once you get the window to open, click on the "install" tab and go ahead and click the "open addons folder" button and place your lightwarp inside. Once done, the lightwarp should show up as an option and all you have to do is click that and then click the "install" button. After that, you can open the game and it should be installed.
<br>
<br>
Here are my results!
<br>
![image](https://github.com/user-attachments/assets/2677988d-a603-424d-a87b-9a98fd8e1980)
<br>
The image shows a comparison between the lightwarps applied. 
<br>
1st image (top left): Default Team Fortress 2 lightwarp in bright light <br>
2nd (top right): Our lightwarp in subtle light <br>
3rd (bottom left): Our lightwarp in bright light <br>
4th (bottom right): Our* lightwarp in complete darkness (light = 0). <br>
<br>
In the case of the 4th picture, my character is standing in a spot in the map where 0 light properties are hitting it. While there is light all around me, and my character is seemingly touching an area where there is light, due to the character's hitbox standing on the spot with no light, my whole character's lightwarp effect is not shown. 
<br>
<br>
It all depends on the light!!
<br>
<br>
If you've followed the guide correclty, you should be able to create and apply your own custom-made lightwarps onto Team Fortress 2.
