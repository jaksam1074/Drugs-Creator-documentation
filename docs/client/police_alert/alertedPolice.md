Triggered when police is alerted 

## Event
``` lua
RegisterNetEvent("esx_advanced_drugs:alertedPolice", function(coords)

end)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                             |
| `coords`          | vector3    | Coordinates where a player tried to sell drugs  |

## Example
``` lua
-- Disables the default police alert
RegisterNetEvent("esx_advanced_drugs:esx:ready", function() 
    exports["esx_advanced_drugs"]:disableScriptEvent("esx_advanced_drugs:alertedPolice")
end)

RegisterNetEvent("esx_advanced_drugs:alertedPolice", function(coords)
    -- Do something
end)
```