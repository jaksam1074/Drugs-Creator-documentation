Used to show the usual `Press E to ...` at the top left of the player's screen

## Export
``` lua
exports["advanced_drugs_creator"]:replaceShowHelpNotification(customFunction)
```

### Parameters

| Name              | Data Type | Description                 |
| -                 | -         | -                             |
| `customFunction`         | function    | A function that will replace the default ESX.ShowHelpNotification method. **Requires** the message parameter and will be called each frame |

## Example (you can place it in the folder integrations/cl_integrations.lua of the script)
``` lua
local function myCustomHelpNotification(message)
    -- Customize your function to fit your needs
    print(message)

    ExternalScript.showHelpNotification(message)
end

RegisterNetEvent("advanced_drugs_creator:framework:ready", function() 
    -- This will replace the base function with the one you want
    exports["advanced_drugs_creator"]:replaceShowHelpNotification(myCustomHelpNotification)
end)
```