Triggered when police is alerted 

## Event
``` lua
RegisterNetEvent("advanced_drugs_creator:alertedPolice", function(coords)

end)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                             |
| `coords`          | vector3    | Coordinates where a player tried to sell drugs  |

## Example (you can place it in the folder integrations/cl_integrations.lua of the script)
``` lua
-- Disables the default police alert
RegisterNetEvent("advanced_drugs_creator:framework:ready", function() 
    exports["advanced_drugs_creator"]:disableScriptEvent("advanced_drugs_creator:alertedPolice")
end)

RegisterNetEvent("advanced_drugs_creator:alertedPolice", function(coords)
    -- Do something
end)
```