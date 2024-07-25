
markdown
# Delete Node Modules Script

This script is designed to help manage the deletion of `node_modules` directories within a specified directory.

## Usage

```bash
./npkill <path>
```
or
```bash
bash npkill <path>
```

Replace `<path>` with the directory where you want to search for and potentially delete `node_modules` directories.

## Description

The script performs the following steps:

1. Checks if the input directory path is provided.
2. Searches for all `node_modules` directories under the given path.
3. Writes the list of found `node_modules` directories to `delete.txt`.
4. Asks the user if they want to delete the listed directories (`y`), review them in your default editor (`r`), or skip the deletion (`n`).
5. If the user chooses to delete (`y`), it iterates through `delete.txt` and deletes each directory.
6. If the user chooses to read (`r`), it opens `delete.txt` with your default editor for review.
7. If the user chooses not to delete (`n`) or if no `node_modules` directories are found, appropriate messages are displayed.

## Example

Suppose you have a project directory named `my_project` containing several `node_modules` directories you want to delete. You can run the script as follows:

```bash
npkill my_project
```

This will search for `node_modules` directories within `my_project`, list them in `delete.txt`, and prompt you for further action.

```
All your deleted node modules are listed in delete.txt
Do you want to delete them? (yes/no/review)->[y/n/r]: 
``` 