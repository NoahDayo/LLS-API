# LLS-API

### Request URL:

>https://www.lovelivesupport.com/api.php

### Method：
	
	HTTP GET

### Description：

This API service site is a public welfare operation. 

If you use it, please refer to the document and indicate the data source LLSupport.

*This site uses global https encryption Encryption protocols and other detailed information access SSLLabs query

The developers who need to use this LLS-API indicate that the use is up to warranty LLSupport/LLSIFCE agreement in case not profit.

Application was approved, your information will be recorded.

If you do not apply to use this LLS-API will be automatically blocked by the robot including request ip and devices Agreement to check Application was approve or who was blocked.

Application E-Mail：admin@lovelivesupport.com 

We only accept English/Chinese in Application. The Application Form format Download. 

2015 ~ 2018 Copyright by LLSupport. All rights reserved.

### Documents:

Query Format : 

	/api.php/{type}/{lang}/{page}/{id} if not Return Error
Query Format Card : 
	
	/api.php/card/{lang:jp,cn,en,tw,kr}/{page: [number]/all/info}/{id:[if page = info]->unit_number} 
Query Format Live : 
	
	/api.php/live/{lang:jp[only for jp]}/{page:[number]/info/all}/{id:[if page = info]->live_track_id}
Query Format Event : 
	
	/api.php/event/{lang:jp,cn,inti}
Query Format BeatMaps : 
	
	/api.php/maps/{maps_id [exm:Live_s20003.json]
Query Format Scenario :
	
	/api.php/scenario/{lang:jp,cn,en,tw.kr}/{page:all/info}/{id [if page = info]->scenario_id}
Query Format SubScenario : 

	/api.php/subcenario/{lang: jp,cn,en,kr,tw}/info/{id = unit_number}
Query Format EventScenario : 

	/api.php/eventscenario/{lang:jp,cn,en,tw.kr}/{page:all/info}/{id [if page = info]->event_scenario_id}
Query Format ReleaseKey : 
	
	/api.php/releasekey 



