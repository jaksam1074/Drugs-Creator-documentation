To add a ped to NPC selling blacklist, so players won't be able to sell to the ped (example: blackjack dealers, shop keepers, etc.)



## Event
``` lua
exports["advanced_drugs_creator"]:addPedToNPCSellingBlacklist(ped)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                             |
| `ped`             | ped (integer)    | The target ped's handle  |

## Example
``` lua
RegisterNetEvent('advanced_drugs_creator:esx:ready', function()
    local closestPed = ESX.Game.GetClosestPed()

    exports["advanced_drugs_creator"]:addPedToNPCSellingBlacklist(closestPed)
end)
```