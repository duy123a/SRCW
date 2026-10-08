Everytime the game update, we need to update the CppSDK folder by Dumper-7

1. Clone Dumper-7

https://github.com/Encryqed/Dumper-7

2. Compile it with Visual Studio (hopefully work)

3. Inject it to the game with Process Hacker 2 (Miscellaneous => Inject DLL)

4. It's not work then need to overwrite the offset (no idea how to find the correct offset though)

5. Get a new CppSDK folder (usually at C:/Dumper-7)

If you want to find the IDs for other items, you can locate them in FModel at the following paths:

- Gadgets: UNION/Content/01_Union/Database/Gadget/DT_GadgetData.uasset
- Stickers:
  UNION/Content/01_Union/Database/Sticker/DT_StickerData01.uasset
  UNION/Content/02_Union/Database/Sticker/DT_StickerData02.uasset
- Titles:
  UNION/Content/01_Union/Database/HonorTitle/DT_HonorTitleListDataTable_01.uasset
  UNION/Content/02_Union/Database/HonorTitle/DT_HonorTitleListDataTable_02.uasset
- Horns: A little tricker. The IDs are defined in the EMachineHornType enum class located in UnionSystem_structs.hpp.
  You’ll need to cross-reference it with
  UNION/Content/01_Union/Database/Machine/HornData/DT_HornData_01.uasset
  UNION/Content/02_Union/Database/Machine/HornData/DT_HornData_02.uasset
  in FModel to determine which horn corresponds to each enum name.
