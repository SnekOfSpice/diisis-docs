
Upon activating the plugin in Project Settings, the DIISIS editor will be added to Godot. The DIISIS editor can either be in embedded or windowed mode.

In embedded view, you open the editor like other main screens up top: ![[Pasted image 20260314131110.png]]

In windowed view, you will find a new button in the top right corner of Godot. Click it to open the DIISIS editor in a separate window.
![[Pasted image 20260314131223.png]]

You can change the embed setting in Project Settings > DIISIS > Plugin > View > Embedded.


# UI
## Editor Controls
1. Undo / Redo: Click these buttons to go back and forth between your operations. The label beneath tells you the previous action.
2. Page navigation
3. Add pages
4. Line type selection
5. Line views

![[Pasted image 20260314131629.png]]



## Page Controls
1. Skip Page
2. Incoming references
3. Select / deselect all lines
4. Page Index & Page key
5. Next Page
6. Address Mode to Next Page
7. Page-bound facts

![[Pasted image 20260314131924.png]]

## Line Controls

1. Move line (use shift to move across folders)
2. Add line above/below: Inserts a new line of the selected line type
3. Edit [[High-Level Overview#Facts & Conditionals]]
4. Select & Action menu (copy, cut, paste)
5. Count of references to this line from loopback (LB) and jump page (JP) in choices
6. Delete line

![grafik](https://github.com/SnekOfSpice/dialog-editor/assets/69637995/6e2b77f3-0dab-4c5d-8350-0e6b2df62ddf)

# Setting up the document
**MANDATORY:** [[Text#Actor Names]]

The rest is optional:
- [[Configuring Runtime Method Providers]]

# Exporting
Using the context menu, you can either save the file or use the Save As option to give it a custom name. These output files can be saved anywhere inside ``://res``The last file to be saved in the DIISIS window is the file to be read by the plugin (this can be overridden). Head to [[LineReader & Parser]] to see how to display your work in-game.

![grafik](https://github.com/SnekOfSpice/dialog-editor/assets/69637995/934a59f6-68d1-48a3-bb0a-3663445fd59a)
