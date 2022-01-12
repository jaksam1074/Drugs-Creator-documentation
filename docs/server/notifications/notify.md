Triggered after notifying player server side

## Event
``` lua
AddEventHandler("esx_advanced_drugs:notify", function(playerId, message)

end)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                 |
| `playerId`        | integer    | Target player server ID  |
| `message`         | string    | Message of the notification  |

## Example
``` lua
RegisterNetEvent("esx_advanced_drugs:esx:ready", function() 
    -- Disables the default script notification (otherwise there would be 2 notifications)
    exports["esx_advanced_drugs"]:disableScriptEvent("esx_advanced_drugs:notify")
end)

AddEventHandler("esx_advanced_drugs:notify", function(playerId, message)
    TriggerClientEvent("external_script:notify", playerId, message)
end)
```