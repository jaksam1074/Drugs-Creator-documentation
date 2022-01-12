To remove a ped from NPC selling blacklist, the opposite of the export `addPedToNPCSellingBlacklist`



## Event
``` lua
exports["esx_advanced_drugs"]:removePedFromNPCSellingBlacklist(ped)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                             |
| `ped`             | ped (integer)    | The target ped's handle  |

## Example
``` lua
RegisterNetEvent('esx_advanced_drugs:esx:ready', function()
    local closestPed = ESX.Game.GetClosestPed()

    exports["esx_advanced_drugs"]:removePedFromNPCSellingBlacklist(closestPed)
end)
```