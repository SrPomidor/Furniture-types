This repo contains files for the Furniture addon.

Furniture addon Steam page: https://steamcommunity.com/sharedfiles/filedetails/?id=2909153895

There are two files:
- `.\Furniture\types.xml` file with type definition, count on map, lifetime, etc.
- `.\Furniture\cfgspawnabletypes.xml` file with default item conditions.

And there are two ways how to add these configs to your DayZ server:

Bad way, preferable for masochists: 
- Take some pills for a mental disorder;
- Manually patch your `types.xml` and `cfgspawnabletypes.xml` with the content of this repo;
- Pray all gods to keep your server up and running.
Do not forget to wash your hands after that.

A good way for those who deserve some love and happiness: 
- include addon settings using `CfgEconomyCore.xml` file 
- have a wonderful day, filled with joy, laughter, and love UwU 

General info about CfgEconomyCore and how it works: 
https://community.bistudio.com/wiki/DayZ:Central_Economy_mission_files_modding

So here we go:
0. Ensure you are working within your mission folder.
	For this example, it is `dayzOffline.chernarusplus` folder, but your mission folder may be different.
	
1. Download and unzip this repo.

2. Change `Furniture\types.xml` if needed. 
	You may probably need another `<min>` or `<nominal>` values for your server. 
	Or change `Furniture\cfgspawnabletypes.xml`, if you want to play with the default damage level. By default, all items are "Pristine".

3. Put the `Furniture` folder under your mission folder to have it like `<DayZ server folder>\mpmissions\dayzOffline.chernarusplus\Furniture`

4. Find your `cfgeconomycore.xml` file, it's located in your mission folder: 
   `<DayZ server folder>\mpmissions\dayzOffline.chernarusplus\cfgeconomycore.xml` 
	 and patch it with the following `<ce>` section:  
```xml
<economycore>
	<!-- existing contents of economy core xml -->
	<ce folder="Furniture">
		<file name="types.xml" type="types" />
		<file name="cfgspawnabletypes.xml" type="cfgspawnabletypes" />
	</ce>
</economycore>
```

5. Well done! Have a nice day!
