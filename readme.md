Redwire is a programming language designed for use with Redstone. Redwire is not a compiler, but rather a set of standards.
If you would like to use Redwire you will need to download a seperate compiler.
This is not a guide for new users, but rather a page describing the syntax that Redwire uses.



1. Syntax

Syntax is simple, compared to other languages. Below is a sample function:

path(name:sample, points:a-c, rootblock:redstone_repeater),exitblock:wool>>diverge:midexit>>command_block[Command:/sayhello];

Each function has a type header (in this example path). As of the Prototype it is only there for further expansion, and to allow non-compliant compilers to be able to read compliant code. As of now there is only "path".

Each function defines a path between two points. Other paths can attach to the end and beginning (with the exception of diverged paths). The points definer does this. It defines the beginning as a and c. Another path could have it as c and a.

After some settings, you can see there is a bunch of brackets. These are "path definers" that define the blocks used in the path. Each block faces forward to allow redstone flow. By default blank brackets just place redstone. A block must use the correct Minecraft ID for the block.

Each function must have the points defined, and there may be only one starting and ending point defined. There must be a name as well.

Each path's ending or starting point may be defined multiple times, as much as physically possible by the compiler.

A block may be defined as the exit, or an entrance as long as you define the block in the function. You can define an exit block by using the exitblock configurator. The last block in the operation will be place on top of the block, if you wish to place a block on the side of something you may use the exitsideblock. You can use it for things like redstone torches.

You may attribute NBT data by typing to directly into brackets ([]). In the example we see that we have a command_block with NBT data of [Command:/sayhello].

A configurator definer must have a root option, followed by a colon and the option.

A name must be defined for a path, and a function.

2. Misc.

You may comment out parts by placing text between */ and /*. This will not affect the compilation of redstone.

Compilers may compile to multiple platforms and formats. However, to be compliant you must follow the definitions in this guide. You may make a semi-compliant compiler, that adds new features. In order to have that label you must be able to copy "vanilla" code and have it work properly.

Each function follows one after the other, being separated with semicolons.

Formating is irrelevant, except where data is handled that requires it.