Triggered after notifying player client side

## Event
``` lua
AddEventHandler("advanced_drugs_creator:notify", function(message, uncoloredMessage)

end)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                             |
| `message`         | string    | Message of the notification  |
| `uncoloredMessage`         | string    | Message of the notification but without ~r~, ~g~, etc.  |

## Example (you can place it in the folder integrations/cl_integrations.lua of the script)
``` lua
RegisterNetEvent("advanced_drugs_creator:framework:ready", function() 
    -- Disables the default script notification (otherwise there would be 2 notifications)
    exports["advanced_drugs_creator"]:disableScriptEvent("advanced_drugs_creator:notify")
end)

RegisterNetEvent("advanced_drugs_creator:notify", function(message, uncoloredMessage)
    TriggerEvent("external_script:notify", message)
end)
```