# ToolSave

**ToolSave** is a Python terminal utility designed to help you save unique or complex commands for future use. Rather than scouring the web for commands you know you'll need again, ToolSave allows you to store them conveniently. Commands are saved in JSON format, enabling easy transfer and use across different machines.

## Features

- **Crate your own command categories:** Organise your commands in categories to find them easily the next time you need them.
- **Save Commands:** Store any command that you might need in the future.
- **Easy command reuse:** After saving a command, you wont need to remember it's structure, ToolSave will only ask you for the parts the command needs and execute it with the right sintax.
- **JSON Format:** Easily transferable and compatible with any machine.


## Installation

To install ToolSave, simply clone the GitHub repository and run the install script:

```bash
git clone https://github.com/yourusername/toolsave.git
cd toolsave

chmod +x install.sh
./install.sh
```

## Uninstall

To uninstall ToolSave, simply remove the toolsave alias from the shell configuration file (".bashrc",".zshrc") by deleting the following line, usually placed at the end of the file:

```bash
alias toolsave='cd $SCRIPT_DIR && python3 main.py \"$@\" && cd -'
```
Then removed the cloned directory:

```bash
rm -rf ToolSave/
```


## Usage

To run the tool just write toolsave in your terminal
```bash
toolsave
```

### Create a category

On the main menu, select the second option and enter your categoies desired name.

### Add a command

1. To add a command select a created category. 
2. On the category menu select the "add command" option, and input your command with variable parts enclosed in curly braces {}.

```bash
Enter your command:

mkdir {directory name}
```
This way, when you go to execute the command in the future, when you select it toolsave will ask you for the variables you included in the command and execute it in the right order without you having to remeber:

```bash
Enter the value for "directory name":
```


