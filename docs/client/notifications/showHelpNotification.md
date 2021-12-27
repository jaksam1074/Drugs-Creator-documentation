Used to show the usual `Press E to ...` at the top left of the player's screen

## Export
``` lua
exports["esx_advanced_drugs"]:replaceShowHelpNotification(customFunction)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                             |
| `customFunction`         | function    | A function that will replace the default ESX.ShowHelpNotification method. **Requires** the message parameter and will be called each frame |

## Example
``` lua
-- Placed in esx_advanced_drugs/integrations/cl_integrations.lua

local function myCustomHelpNotification(message)
    -- Customize your function to fit your needs
    print(message)

    ExternalScript.showHelpNotification(message)
end

AddEventHandler("esx_advanced_drugs:esx:ready", function() 
    -- This will replace the base function with the one you want
    exports["esx_advanced_drugs"]:replaceShowHelpNotification(myCustomHelpNotification)
end)
```