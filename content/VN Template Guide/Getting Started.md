# Template
I've used DIISIS in several personal projects ([ex1](https://snekofspice.itch.io/curse-you-entropia) [ex2](https://snekofspice.itch.io/she-was-swallowed-by-the-sun) [ex3](https://snekofspice.itch.io/growing-up)). This template will give you the same game structure as those visual novels, so you don't have to hassle with any coding.

[[Get the Plugin]] to get started. 

# Setting up the visual novel template

## Files
Move the template files from ``res://addons/diisis/templates/visual_novel`` into a separate folder called ``game`` (you have to create this one)

![diisis move files](https://github.com/user-attachments/assets/facaafe3-a937-49dd-b5c6-eefca871f371)

The contents of this folder already contain a minimum project so you can see how a DIISIS file controls the flow of dialogue. This script will be located at ``res://game/diisis_integration/demo_script.json``.

## Automated Setup
In the top right corner, you will find a dropdown menu. 

![grafik](https://github.com/user-attachments/assets/4357f4c9-1fc0-4f95-92bd-70418177196a) 
![grafik](https://github.com/user-attachments/assets/a3351c8f-4656-4b66-b7c9-167e44498e0a)

Confirm the dialogue, and **reload the editor.**


# Visual Novel Structure
This section explains all the different folders and scenes contained within.

## autoloads

The demo project comes with some autoload singletons.

### const
`CONST` is a simple container that holds paths to all of your assets. All asset types are defined by a root they all have to share, and their name within that root folder. If you want to add more screens, backgrounds, sounds, sfx, or stages, this is where you reference them.

![grafik](https://github.com/user-attachments/assets/fa0d8e86-04e1-4270-9865-11e9f6772edb)

If you declare new assets here, they have to be a character-exact match (but not case-exact) to the string you pass in the provided functions in DIISIS.

![grafik](https://github.com/SnekOfSpice/dialog-editor/assets/69637995/bbf51f19-cde4-4454-9915-f60ff03e599b)
![grafik](https://github.com/SnekOfSpice/dialog-editor/assets/69637995/8424e8ea-d1d0-4c90-8b7a-9603efa95086)



### game_world, options and sound
These are not really meant to be drilled into. Feel free to look around, but you don't need to adapt them.

``Options`` determines the default behavior for settings though.

![grafik](https://github.com/user-attachments/assets/f587dcdf-4060-478f-9578-40cc7b75c89c)


## backgrounds
Backgrounds are .png or .tscn files that can be switched to with certain [[Instruction]]s in DIISIS.

## cg
CG is a visual novel-specific term for typically full-screen renders. Pretty!

## characters
`character.tscn` is a class to display a character in your visual novel. A small rundown on how to add your own can be found [[Creating New Characters||here]].

These nodes require a ``character_name`` to be set to display their respective emotions.

![grafik](https://github.com/user-attachments/assets/768dc0f2-5c6a-4908-95b1-a02caa6e69ce)

These names correspond to the names declared in the character dropdown within DIISIS.

![grafik](https://github.com/user-attachments/assets/f458aa5d-adb5-4657-b818-cc64087176d6)


Within the `sprites` folder, you will find all the emotions that the characters in the demo express. They correspond to the respective stringkits too. The naming scheme for character sprites is `[character name]-[emotion name]`, and the individual stringkits (e.g. amber-emotion) are named `[character name]-emotion`. The ``character.gd`` script will automatically find the correct sprites if you follow these conventions within the project.

**Files:**

![grafik](https://github.com/user-attachments/assets/011f999d-5a43-475e-b054-bcb6ef3798fb)
![grafik](https://github.com/user-attachments/assets/e7985d30-6638-49a9-820b-617bf70b35ae)

**Syntax:**

![grafik](https://github.com/user-attachments/assets/4adcb0c4-1fdb-496d-9e76-4acd0086c407)


## screens
Screens are like menus. Only one of them can be active at a time, and they can be closed with escape or mouse input. Here you have e.g. an options menu or the content warning notice.

## sounds
Folder for music and other SFX. Don't forget to reference them in `CONST`.

## stages
Stages are the big changes. In the demo, you get the main menu, and game stages.

### game_stage
If you adapt the demo, and add more features, you might want to look into `game_stage.gd`. It has two functions for serialization and deserialization respectively. So if you have some game element in this stage that needs to persist between save states, this is where you handle it.

Furthermore, the game stage comes with an option between two styles of text box placement. ToBottom places the text box statically at the bottom of the screen. ToCharacter lets the text appear next to the respectively speaking character.

![grafik](https://github.com/SnekOfSpice/dialog-editor/assets/69637995/fb4e74e2-05d5-4f42-a95f-a4ee90c90599)


## visuals
A folder I use for various icons, fonts, themes, etc.

## DIISIS instructions
Call these with [instruction lines](https://github.com/SnekOfSpice/dialog-editor/wiki/Line-Type:-Instruction) to do typical visual novel stuff.

![grafik](https://github.com/user-attachments/assets/199b3f83-2c97-49b4-a815-5606f6bc0956)


# Learning DIISIS

Head over to the [Quick Start Guide](https://github.com/SnekOfSpice/dialog-editor/wiki/Editor-Overview) to get a feeling for the dialog editor.
