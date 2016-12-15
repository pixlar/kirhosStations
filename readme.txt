Adding a room: Rooms are 34 x 18 blocks. The room included here uses spawners so that the npcs respawn if they die. The room must also be patched into the .dungeon file for each station it spawns on. Please check the numbers in this mod to get an idea of how often the racial rooms spawn; its a little weird if a Hylotl station is filled with Floran rooms.

Adding a station: Stations should include a stationmanager stagehand, spaces for common rooms, defense lasers, enemy lasers, alarms, and stationspeakers. These are not required, but they allow events to occur on your station. Events are patched onto stations in the /stagehands/events/stations.config file, which also defines the species for a station.

Adding a visiting ship: The images for a visiting ships are tier 3 ships. The image for your ship should be placed in objects/m4_stations/visitingship. It should be named <race>ship.png. Your shiptype and crew should be patched into the visitingship object in the same it is for this mod.

Adding an event: the event included in this submod is a "raider" event. The script is included in the spacestations mod itself. 
Events are controlled by stagehands and the scripts attached to them. Once you have built the script for an event, create a new stagehand with the script attached. Events are patched onto stations in the /stagehands/events/stations.config file
Station Manager Functions
The stationmanager stagehand controls various parts of the station. Using world.sendEntityMessage you can trigger these functions easily.
	stationlasers, toggle
		toggle can be set to true or false. This sets the station's weapons to fire randomly.
	enemylasers, toggle
		toggle can be set to true or false. This sets enemy weapons to fire randomly at the station. This is not included on every station and will not do anything on stations without enemylasers
	alarms, toggle
		toggles all the station alarms on or off. Alarms may vary by station.
	broadcast, msg
		commands all speakers on the station to say msg.