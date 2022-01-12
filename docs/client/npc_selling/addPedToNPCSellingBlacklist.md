To add a ped to NPC selling blacklist, so players won't be able to sell to the ped (example: blackjack dealers, shop keepers, etc.)



## Event
``` lua
exports["esx_advanced_drugs"]:addPedToNPCSellingBlacklist(ped)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                             |
| `ped`             | ped (integer)    | The target ped's handle  |

## Example
``` lua
RegisterNetEvent('esx_advanced_drugs:esx:ready', function()
    local closestPed = ESX.Game.GetClosestPed()

    exports["esx_advanced_drugs"]:addPedToNPCSellingBlacklist(closestPed)
end)
```