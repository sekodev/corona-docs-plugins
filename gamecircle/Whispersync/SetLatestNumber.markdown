# gamecircle.Whispersync.SetLatestNumber

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [function][api.type.function]  
> __Library__           [gamecircle.*][plugin.gamecircle]  
> __Return value__      None  
> __Revision__          [REVISION_LABEL](REVISION_URL)  
> __Keywords__          Latest, SyncableNumber, Whispersync  
> --------------------- ------------------------------------------------------------------------------------------


## Overview
Set a value to the latest number associated with the key. Only the latest value assigned will be stored. 


## Syntax
	gamecircle.Whispersync.SetLatestNumber(key, value, NT_constant)
	gamecircle.Whispersync.SetLatestNumber(key, value, NT_constant, metadata)
	
##### key ~^(required)^~
_[String][api.type.String]._ The key used to access a specific latest number.

##### value ~^(require)^~
_[Number][api.type.Number]._ The value to be assigned to the latest number.

##### NT_constant ~^(required)^~
_[String][api.type.String]._ The NT_constant, which is either "INT" or "DOUBLE", determins how the latest number will be stored. "INT" cutt off the decimal value. "DOUBLE" maintain the decimal value intact. If the string given is invalid, "INT" will be used by default.

##### metadata ~^(optional)^~
_[Metadata][plugin.gamecircle.Whispersync.Metadata]._ A table of metadata to be stored with the number. It must be a lua table comprised only of string fields with string values in those fields. For examples and more information, check the documentation page for metadata. 

## Examples

``````lua  
local latestNumKey = "myFirstLatestNumber" 
local gamecircle = require("plugin.gamecircle")  
gamecircle.Init(false, false, true)  
gamecircle.Whispersync.SetLatestNumber(latestNumKey, 10, "INT")  
gamecircle.Whispersync.SetLatestNumber(latestNumKey, 1000, "INT")  
gamecircle.Whispersync.SetLatestNumber(latestNumKey, 1, "INT")  
gamecircle.Whispersync.SetLatestNumber(latestNumKey, 10000, "INT")  
gamecircle.Whispersync.SetLatestNumber(latestNumKey, 100, "INT")  
print("The Latest Number is: " .. gamecircle.Whispersync.GetLatestNumber(latestNumKey, "INT").value)  
print("These are all the Latest Number values stored under the current GameData set of Whispersync.")  
local keys = gamecircle.Whispersync.GetLatestNumberKeys()  
for i,key in ipairs(keys) do   
	print("-" .. key)  
end  
``````
