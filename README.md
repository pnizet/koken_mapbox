koken_mapbox
============
Hello all,
I would like to share with you a customization that I've done on my koken installation and that lots of you would like to have (I'm prety sure of it).
A map with all your pictures on it.
I choose to use OpenStreetMap, an open project rather than google maps and it's closed environment by faith, and because their maps are nicer. 

First of all I would like to precise that web dev is not my job, i've done this with my little knowledge of web dev and I'm pretty sure that there is a lot of improvement that can be done. But it works, if you have suggestions, I will be pleased to read them.

So here is the method :
- First create an account on MapBox.com (it's free, if you'are not displaying more than 3000 maps/month), Create a project, it will give you a "Map ID"
- Download the called map.lens
- Replace in the code YOUR_MAP by your "Map ID"
- Save the file / Upload the file to /storage/theme/your_theme/

Configuration of the map
- It will display 250 markers (max loop), you can change the number of markers displayed by changing the line 51
- If you left the code untouched the map will be centred on the median coordinate of all the markers (I've done this because most of my pictures are in France, a few are in Australia... showing a map that fits to all the markers was quite weird)
- If you prefer to display a map that fits all the markers uncomments line 197 to 199

That's all !

If you would like to see it in action you can go to his page : http://pierre-nizet.fr/carte/
