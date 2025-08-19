# GrandFantasia-UI-Editor
A modern, browser-based tool for visually editing the user interface (.xml) files for the game Grand Fantasia. Built with modern web technologies, this editor provides a real-time, intuitive interface to manipulate UI elements, textures, and properties, streamlining the UI modding process without needing to install anything. Everything is done locally in your browser and no files are upload to a server.

<img width="2560" height="1440" alt="image" src="https://github.com/user-attachments/assets/0e6a3d0f-8d64-4bb0-aa1c-82a2d19df2f0" />

## Usage
1. Either open this link to open <a href="https://ahmetakyuez.github.io/GrandFantasia-UI-Editor/">UI-Editor</a> in your browser directly or download the .html file locally and open it in your browser.
2. Click the "Select UI Folder" button and choose the root UI directory from your Grand Fantasia game client.
3. Your browser will ask for permission to view and save files in this folder. You must grant permission for the editor to work correctly.
4. Once the folder is loaded, the file list on the left will populate. Click on any .xml file to begin editing
5. Use the various panels and tools to make your changes.
6. Click the "Save Changes" button when you are finished.

## Key Features
- **Automatic Backups & Versioning**: Never lose your work. When you save, the tool automatically creates a timestamped backup. You can easily view and restore previous versions, including the original file, directly from the editor. This tool creates a new folder in your UI folder, UI-Editor which saves the original `.xml` files and your modded versions. <br> <img width="391" height="363" alt="image" src="https://github.com/user-attachments/assets/91415ddf-2e60-4c9c-9f61-979955c16ae7" />
- **Visual UI Editor**: Render .xml UI files in a canvas with their corresponding textures that you can pan and zoom. Quickly spot imperfect texture coordinates<br><img width="766" height="293" alt="image" src="https://github.com/user-attachments/assets/cdee8132-9a7c-43d2-97d5-2377a8321d00" />
- **Element Editor**: Select elements with your mouse for direct manipulation. You can also quickly visualize the UV map and change the coordinates <br> <img width="361" height="294" alt="image" src="https://github.com/user-attachments/assets/18765523-b6ae-473c-b01c-32e2bdf3bf49" />
- **Hierarchy Inspector**: View the complete tree structure of all UI elements. You can easily select, multi-select, hide, isolate, and navigate complex UI layouts.
- **Property Editor**: Make precise adjustments to any selected element's position, scale, font size, and texture coordinates (UVs) through a simple input panel.
- **Raw XML Editor**: A dedicated tab to view and edit the raw XML source code directly, offering full control for advanced users.
- **Texture Inspector**: Automatically lists all textures (.dds files) used for the current loaded UI element. A popup viewer shows the texture atlas and highlights which elements use which part of the texture. <br> <img width="383" height="221" alt="image" src="https://github.com/user-attachments/assets/d4a62e16-03c7-4255-923c-6101fc63c9ab" />
- **Quick Rescale**: Lets the user quickly rescale all elements of a .xml file e.g. to increase the user-friendliness of the game interface for high resolution monitors. <br> <img width="400" height="287" alt="image" src="https://github.com/user-attachments/assets/8f3d33ec-cfdc-40aa-96c2-bdc95c6a6fff" />
- **Global Font Editor**: A specialized tab that lists every element with a font property, allowing you to view and modify all font sizes in one convenient location.

## Known Bugs / Missing features
This is a list of current bugs that I am aware of and a list of features that I want to implement in the future.
- The Font-Editor tab is not working
- Hierarchy Inspector is not correctly matching Children to their parents as it did in a previous version.
- Some .xml files cannot be loaded
- Some UV textures are not loaded in correctly
- Preview mode is not centered
- Grouping/Categorization of .xml files can be improved

## Planned features
- Some elements cannot simply be changed in their scale e.g. the `inventory.xml`. My guess is that this is because these UI elements are changed dynamically by functions which have their sizes written statically. Interface elements which are static in their layout and in their number of elements can be scaled without any problems e.g. the `ShortcutBar.xml`

## Quick Guide to increase elements Size:
1. Open the tool as described above
2. Open an element and click the rescale button in the toolbar <br> <img width="1876" height="542" alt="image" src="https://github.com/user-attachments/assets/02d49abc-f03f-44b6-9d71-83ed11e03629" />
3. Enter in a value and click save.
4. Restart the game to fully reload the UI

### List of files that I highly recommend to increase in size:
I would generally recommend you to increase most of the elements as you want as the process is extremely quick and simple to test. Do note that some elements do not work properly when scaled e.g. `inventory.xml` because the amount of elements/boxes is not static.
- `Menu.xml` This is your main hotbar
- `Shortcut.bar` This is your additional skillbar
- `Radar.xml` This is your minimap on the top-right of your screen
- `BasicChar.xml` This is your main character status on the top left of your screen
- `Equipment.xml` This is your character Sheet (Hotkey C)
- `FullEnchantList.xml` This is the bar which shows _all_ the buffs.
- `QuickEnchantList.xml` This is the bar which shows the buffs which are running out.
- `ElfWork.xml`This is the list of your Sprites which opens when you want to craft something. <img width="861" height="658" alt="image" src="https://github.com/user-attachments/assets/81c216b6-a751-4b42-bd03-124ca4688f11" />
- `Diary_QuestLog.xml` This you Questbook / Adventure Log (Hotkey L).
- `MailList.xml` These are your Messages from e.g. Auctions
- `Shop.xml` This is your Menu to buy
- `GameItemWiki.xml` GF-Violet / This is your In-game Wiki (Hotkey H)

### List of files that do not scale properly (not complete):
- `ElfUI.xml`
- `Inventory.xml`
- `ElfInventory.xml`
- `Storage.xml`
- `WorldMap`
