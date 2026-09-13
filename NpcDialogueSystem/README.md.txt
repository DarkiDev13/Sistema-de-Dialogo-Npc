# Sistema de Dialogo

Sistema de Dialogo desarrollado en Roblox Studio utilizando Luau.

## Características

- Dialogo configurable
- Soporte para diferentes Npc's
- Uso de RemoteFunctions
- Separación entre cliente y servidor

## Tecnologías

- Roblox Studio
- Luau
- RemoteFunctions
- ModuleScripts

&& Scripts/Folders/Interfaces

DialogoCliente --> StarterPlayerScripts
DialogoUI.lua --> DialogoCliente
Utils --> ReplicatedStorage
NpcsData --> Utils -> Data.lua
GUIFX.lua --> Utils
Remotes --> ReplicatedStorage
NpcServices --> ServerScriptService
NpcInteraction.lua --> NpcServices
Dialogue --> ScreenGui

DialogoCliente: LocalScript; Manejo del Interfaz de Usuario y Respuestas Al Interactuar con la Interfaz.

NpcsData.lua: ModuleScript; Tabla de datos de los Npcs los cuales son interactuables. Contienen el dialogo en formato %STR%
dentro de la tabla del NPC la cual es una tabla con una KEY asignada dependiendo el .Name del NPC

GUIFX.lua: ModuleScript; Efectos para las interfaces del usuario

NpcInteraction.lua: ServerScript; Valida y Detecta el Proximity Prompt cuando es ejecutado por el jugador, manda un INVOKECLIENT y
lo manda al DialogoUI.lua