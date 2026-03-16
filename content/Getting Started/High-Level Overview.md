# Editor & Parser
DIISIS has two core components:
1. Editor: An [[Editor Overview|editor]] to create a JSON file.
2. Runtime: That file is then loaded into memory by the Parser autoload and can be traversed and displayed with a LineReader node. See [[LineReader & Parser]].

![grafik](https://github.com/user-attachments/assets/cec562c6-6bb1-4532-b61f-7bfa4c12578d)


# Pages & Lines
DIISIS is structured into Pages and Lines. These are rough guides for laying out the structure of your document. Generally, you want to use pages for isolated scenes, then fill them with lines.

![grafik](https://github.com/user-attachments/assets/49e86174-5b70-4e3a-b52e-f7eba78e669d)

Lines can have one of four types:
* [[Text]]: Displays text to the screen, using a bespoke syntax.
* [[Choice]]: Offers choices to the player. Can also be used to implictly switch pages.
* [[Instruction]]: Calls functions to interact with the rest of the game.
* [[Folder]]: Structures lines into groups to assist with reactivity in-game and readability in-editor.


# Facts & Conditionals
DIISIS comes with a fact system. For any page, line, or choice item, you can declare any fact to become `true` or `false`, or any integer when that point of the dialog is reached. Note that you cannot switch data types for a fact.

With conditionals attached to individual lines or choice items, you can make the game reactive to player decisions.