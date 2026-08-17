Rollback is a feature common to many visual novels, allowing you to go back to a previous line of dialogue without consulting the history. DIISIS also has this feature in full, as of 0.9.


## Configuration
Parser allows you to configure blocking points for the rollback. If you want Folders or Choices to stop the player from going further back, you can toggle those in the exported properties.

## Adding Rollback to your project
Some features are not added by default, tho they can be added fairly simply yourself. For instance, facts are not restored to their state when going by rollback, but the VN Template comes with an autoload to handle just that.


## Warnings & Incompatibilities
Some features of DIISIS are not compatible with rollback, or require some additional coding work from you. Especially with ``LineReader.keep_past_lines`` enabled, it would require extensive code work on your end to facilitate rollback.


## Implementation Details
(as of DIISIS 0.9)
Parser logs all addresses it has visited, linearly. When requesting a rollback, it either goes to the previous subline index of the current [[Text]] Line, or the previous Text Line if at the beginning of the text line. It will skip over all Folders, Choices, and Instructions, although it will execute [[Instruction#Reverse Instructions|Reverse Instructions]] in backwards order.