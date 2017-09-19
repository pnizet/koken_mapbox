koken_mapbox
============

A "kind of" plugin for koken CMS which integrate Mapbox map and groups markers in clusters


First of all I would like to precise that web dev is not my job, i've done this with my very little knowledge of web dev and I'm pretty sure that there is a lot of improvement that can be done. But it works, if you have suggestions, I will be pleased to read them.

## So here is the method to use it:
- Download the files
- First create an account on MapBox.com (it's free, if you are not displaying more than 3000 maps/month)
- Create a Token in the API access Token section
- Replace in the code YOUR_TOKEN by your token 
- If you want a specific map, Create a project, it will give you a "Map ID", Replace in the code YOUR_MAP by your "Map ID"
- If you want to use the standard MapBox maps you can replace YOUR_MAP by ``mapbox.dark`` or ``mapbox.outdoors``
- Save the file / Upload the file to /storage/theme/your_theme/
- you can acces to your map directly by the url YOUR_KOKEN_URL_HOME/map

## Configuration of the map
- You could maybe have an issue with the first line of the file map.lens. If so replace ``inc/header.html`` by ``layouts/header.html``
- ~~If you left the code untouched the map will be centred on the median coordinate of all the markers (I've done this because most of my pictures are in France, a few are in Australia... showing a map that fits to all the markers was quite weird)~~ not working any more with the json loading
- ~~If you prefer to display a map that fits all the markers uncomments line 197 to 199~~ not working any more with the json loading

## With some additions (thanks to lvillard):
- it uses spiders on the lower zoom level when pictures share the same coordinates (see the section "// Mapbox spiders")
- the height of the map will be reduce if the screen is less than 766px (for mobile phone)
```css
#map_full { top:0; bottom:0; width:100%; height: 450px; margin-top: -5px;}
@media screen and (min-width: 766px) {
	#map_full {
	display: inline-block;
	height: 1000px;
	width: 100%;
	}
}
```

That's all !

If you would like to see it in action you can go to his page : http://pierre-nizet.fr/carte/
