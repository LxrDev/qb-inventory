# Qb-Inventory + [UI]

```
print ("Dont Forget That All Rights For LXR DEV ! 🧾 ")
```

# [Steps:]

# To Avoid The Problems And Cmd Crashes Delete The -main word- --> 'qb-inventory-main' --> 'qb-inventory'

* Download `qb-inventory`
* Drag `qb-inventory` into your scripts folder
* You have to delete the [main] word --> 'qb-inventory-main' --> 'qb-inventory'

-------------------------------------------------------

# [Requirements:]

* [qbcore framework](https://github.com/qbcore-framework)
* [qb-target](https://github.com/BerkieBb/qb-target)
* [qb-core](https://github.com/qbcore-framework/qb-core)
* [qb-logs](https://github.com/qbcore-framework/qb-logs)
* [qb-traphouse](https://github.com/qbcore-framework/qb-traphouse)
* [qb-radio](https://github.com/qbcore-framework/qb-radio)
* [qb-drugs](https://github.com/qbcore-framework/qb-drugs)
* [qb-shops](https://github.com/qbcore-framework/qb-shops)

# [Add This Snippet If You Dont Have It In qb-core/server/player:] 👇

function QBCore.Functions.AddPlayerMethod(ids, methodName, handler)
    local idType = type(ids)
    if idType == "number" then
        if ids == -1 then
            for _, v in pairs(QBCore.Players) do
                v.Functions.AddMethod(methodName, handler)
            end
        else
            if not QBCore.Players[ids] then return end

            QBCore.Players[ids].Functions.AddMethod(methodName, handler)
        end
    elseif idType == "table" and table.type(ids) == "array" then
        for i = 1, #ids do
            QBCore.Functions.AddPlayerMethod(ids[i], methodName, handler)
        end
    end
end

-------------------------------------------------------

# You Can Find Us On :

Our [Discord](https://discord.gg/R9KgyCkXJp) for updates, support.

-------------------------------------------------------

# [Showcase:]


