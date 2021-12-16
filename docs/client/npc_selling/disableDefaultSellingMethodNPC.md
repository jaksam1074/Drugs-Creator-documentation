Trigger to disable the prompt above NPCs "Press E to sell drugs"
<br/><br/>
If you disable the prompt, you have to manually trigger the ```esx_advanced_drugs:sellToNPC``` event to sell to NPCs

## Event
``` lua
TriggerEvent("esx_advanced_drugs:disableDefaultSellingMethodNPC")
```

## Example
``` lua
-- Disables the prompt
RegisterNetEvent("esx_advanced_drugs:esx:ready", function() 
    TriggerEvent("esx_advanced_drugs:disableDefaultSellingMethodNPC")
end)

-- Manually sell to an NPC (example for targeting scripts)
Citizen.CreateThread(function() 
    local closestPed = ESX.Game.GetClosestPed()

    TriggerEvent("esx_advanced_drugs:sellToNPC", closestPed)
end)
```