Triggered after notifying player client side

## Event
``` lua
AddEventHandler("esx_advanced_drugs:notify", function(message, uncoloredMessage)

end)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                             |
| `message`         | string    | Message of the notification  |
| `uncoloredMessage`         | string    | Message of the notification but without ~r~, ~g~, etc.  |

## Example
``` lua
RegisterNetEvent("esx_advanced_drugs:esx:ready", function() 
    -- Disables the default script notification (otherwise there would be 2 notifications)
    exports["esx_advanced_drugs"]:disableScriptEvent("esx_advanced_drugs:notify")
end)

RegisterNetEvent("esx_advanced_drugs:notify", function(message, uncoloredMessage)
    TriggerEvent("external_script:notify", message)
end)
```