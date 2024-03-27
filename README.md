# Hed ![pencil-icon](https://github.com/jgyo/hed/assets/2886615/d23d8ffc-1b28-4dad-b37f-9ec6d33096b8)
An HDL editor for use with [From Nand to Tetris](https://www.nand2tetris.org/)
HDL files.

From Nand to Tetris is a project by Noam Nisan and
Shimon Schocken to enable "students, instructors, and self-learners"
everything they need to know to build a "general-purpose"
computer from scratch. The site I have linked above provides
most of the materials needed for that endeavor, except
for an HDL editor. That's where **Hed** comes in.

I decided to write **Hed** when I started a video
series based on Nand2Tetris to help users edit these files.

The program is easy to use. Download the
[latest release,](https://github.com/jgyo/hed/releases) unzip it, and execute one of the install
files to install the program. You may receive a warning about
installing software from "unknown sources." Please ignore those
warnings to complete the install.

When you first run **Hed** it will look like this:

![image](https://github.com/jgyo/hed/assets/2886615/126182be-0233-4618-84bf-d228b55d0d04)

The first thing you should do at this point is to open the "Settings" window by clicking
on "Settings" and then "Resources."

![image](https://github.com/jgyo/hed/assets/2886615/06af48bd-3ab4-4cf2-a694-9ff30aa70a60)

You will see another window that looks like this:

![image](https://github.com/jgyo/hed/assets/2886615/da51e25a-da04-4bea-827a-310531fd1fc2)

At a minimum, select a "default save folder" in the "Save folder" field. You can use the "Select"
button to its right to open the folder browser to find the folder you want to use. Normally
you would choose one of the project folders from within the Nand2Tetris resource directories
that you would get from Nisan's and Schocken's site above. I am referring to the fourteen
numbered folders under the "projects" folder.

![image](https://github.com/jgyo/hed/assets/2886615/6c5e60f3-a26d-4fb0-958d-727f1265b3c8)

Completing the rest of the fields in the window is useful but not necessary.
For example, the "Components folder" field specifies a directory where preexisting
components might be found. I use this to point to the Nand2Tetris "builtInChips" folder.

![image](https://github.com/jgyo/hed/assets/2886615/2fdf3053-c188-4fb0-b2cf-1c2f1558014a)

Once you are satisfied with your changes, click on the "Save" button on the bottom
right of the window. Otherwise, the settings will not be saved for the next time you
execute **Hed.**

Now you can really start using **Hed.**

Back in the main window, open the "File" menu and click "Open." You should see an
"Open an hdl file" window opened on the directory you selected as your default
save folder in the "Settings" window. From this window, you can open any available HDL
file.

I have opened the "Not.hdl" file in the following screenshot.

![image](https://github.com/jgyo/hed/assets/2886615/e35163b9-e191-4165-96b4-13f62ffb02f7)

The "Not" gate is just about the simplest logic gate, so there isn't much to
see in this window. But you should see a couple of changes. First, the name of the gate
is now specified in the "Gate Name" field, and one input pin called "in" is specified
in the grid below the seven tab headers right below the "Gate Name."

"Input Pins" is highlighted, meaning we are looking at input pins in the grid below.
The "Not" gate has only one input pin. The gate also has only one output pin called
"out." But on the "Parts" page, zero parts are specified.

![image](https://github.com/jgyo/hed/assets/2886615/a4fa352a-1863-4780-ac46-a456525d395d)

That's because the file we loaded is only a stub file. It provides the inputs and
outputs, and describes what the logic gate is supposed to do, but it is left for someone
else to supply the details about its implementation.

I will do that now to show it. First, I click within the cell below "Name" and type
the letter "N." (HDL is case sensitive, so it's important to consider capitalization
here. Most preexisting gates in Nand2Tetris start with capital letters. Typing a
lowercase "n" here would not produce the same results.)

![image](https://github.com/jgyo/hed/assets/2886615/99307b6c-68fa-4cc6-b85e-4baef1ac83dc)

A list of logic gates that **Hed** knows about starting with the letter "N" appears.
At this point, the only defined gate in the list is the "Nand" gate, which we
will use to create the "Not" gate.

We can either select the "Nand" gate from the list or type out "Nand" to select
it. From the "Name" cell, we can tab over to the "Description" cell to give some detail about
it. This is the only gate we need for "Not," so we say so.

![image](https://github.com/jgyo/hed/assets/2886615/f1731077-ae38-4800-8c01-16da58141611)

We have to use the grid on the right to edit the part's connections. With the "Nand" part
selected on the left, click on the row that says, "Click here to add a new row" in the
"Selected Part Connections" grid.

![image](https://github.com/jgyo/hed/assets/2886615/a3509a55-bcbb-4a3b-9d62-62c8ce788798)

Now we can start editing here.

Under "Part Pin," we will type "a" to specify one of the "Nand's" inputs and then press
the tab key to move to the "External Pin" column. This column is where pins external to the
selected part are specified. In this case, we want to specify the logic gate's "in" pin,
so we type "in" and press tab key again.

The "Nand" gate has two inputs. We are going to tie the "Not's" input pin to both of those pins,
so for the second row, we type "b," tab, "in," and tab once again.

You might notice a change under "Connections" now on the left. The "Connections" column
on the left is non-editable; it reformats the data you enter in the second grid so it can
be seen whether the row is selected or not.

We still have a little more work to finish the "Not" gate's connections, which
is to hook up its out pin. If necessary, click on the bottom row under "Part Pin"
in the second grid. Then type "out," tab, and then "out" again. Here the
first "out" refers to the "Nand" gate's out pin, and the second "out" refers to
the "Not" gate's out pin.

![image](https://github.com/jgyo/hed/assets/2886615/30195557-5ac9-4492-8cbe-f85e2208cc48)

The "Header Text," "API Text," and "Description Text" pages contain whatever was in
the original HDL stub file we loaded at first. For now, we won't make any changes
there. But let's look at the "File View" tab.

![image](https://github.com/jgyo/hed/assets/2886615/c1bad184-d379-41ef-a161-89473f0c849c)

There's our completed HDL file, including the changes we made under the "PARTS"
section. All we need to do is save the file, and we will be ready to load
the file up in the Nand2Tetris Hardware Simulator and run tests to see if it works
as expected.

Saving is accomplished by clicking on the disk icon in the window's upper right.
**Hed** will save the file to a file named "Not.hdl" (named after the logic gate's
name) directly in the default save directory you specified in the "Settings" window.
Since that's the directory from which we loaded the original "Not.hdl" file, that file will
be overwritten with our changes. If that is not your intent, you should save a copy
of the original to another location before saving the changes to the file.

Well, that's about it. I have included a Users Guide for **Hed** in the install directory
but, honestly, I don't think you will need it. I hope you enjoy this tool, and
that it helps in your study of logic gate design.
