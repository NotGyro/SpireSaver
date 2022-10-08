# SpireSaver
This is a command-line Slay the Spire save file 
deobfuscator / reobfuscator that I threw together in a couple of hours. 

I used andrewsnyder328's SaveEditor.kt file for reference, but the style 
of this tool is pretty different from that one (of course, it has to be - 
Rust and Kotlin do not have much in common). 

# Building
Simply use `cargo build`, or `cargo run` to run it directly. 
If you do not have Cargo installed, one good way to install
it is [Rustup](https://rustup.rs).

# Usage
First, run ``./spire_saver <input_file> <output_file> deobf``, 
where <input_file> is a Slay the Spire savegame file taken directly 
from the `saves` subdirectory in your `SlayTheSpire` installation directory. 
That file's name will probably be something along the lines of IRONCLAD.autosave, 
DEFECT.autosave, SILENT.autosave, etc.

For your output, <output_file> can be whatever you want.
Then, open up your output file. It should be in plain, readable json. 
Make whatever edits you wanted to make, and then save that file.

Next, run ``./spire_saver <edited_file> <final_file> obf``.
This will reobfuscate your save data. Take the generated <final_file>
(which, again should follow the form of DEFECT.autosave, or SILENT.autosave,
or something along those lines), and put it back in Slay the Spire's `saves`
directory. You should be all set!
