# Предполагаемые подсистемы

## Runtime / memory

Основание:

- `NtAllocateVirtualMemory`
- `NtProtectVirtualMemory`
- `NtFlushInstructionCache`
- `VirtualProtect`
- `NtCreateThreadEx`

Вывод:

DLL использует нативный рантайм с управлением памятью, защитой страниц и собственными потоками.

## Graphics / UI

Основание:

- `d3dx9_43.dll`
- `D3DXCreateTextureFromFileA`
- `D3DXCreateTextureFromFileInMemory`
- крупная секция `.rsrc`

Вывод:

Внутри есть встроенные графические ресурсы и UI-часть, использующая DirectX 9.

## Network

Основание:

- `WS2_32.dll`
- `MSWSOCK.dll`
- HTTP-строки
- `Lost connection to Neverlose servers.`

Вывод:

Присутствует отдельный сетевой слой для связи с backend или shared-функциями.

## Lua scripting

Основание:

- `Lua Editor`
- `Scripts`
- `Documentation`
- `Auto Reload`
- `Copy Lua Path`

Вывод:

DLL содержит подсистему управления Lua-скриптами со встроенным интерфейсом.
