Trigger to start selling to an NPC, as you would do after pressing E to sell in the default method

## Event
``` lua
TriggerEvent("esx_advanced_drugs:sellToNPC", ped)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                             |
| `ped`             | ped (integer)    | The target ped's handle  |

## Example
``` lua
local closestPed = ESX.Game.GetClosestPed()

TriggerEvent("esx_advanced_drugs:sellToNPC", closestPed)
```