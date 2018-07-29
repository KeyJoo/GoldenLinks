# Terminal: delete not empty folder

https://askubuntu.com/questions/217893/how-to-delete-a-non-empty-directory-in-terminal
- `rm -rf folderName`
- `sudo rm -rf folderName`

Otherwise, without sudo you will be returned permission denied. And it's a good practice to try not to use -f while deleting a directory:

`sudo rm -r folderName`

Note: this is assuming you are already on the same level of the folder you want to delete in terminal, if not:

`sudo rm -r /path/to/folderName`

FYI: you can use letters -f, -r, -v:

    `-f` = to ignore non-existent files, never prompt
    `-r` = to remove directories and their contents recursively
    `-v` = to explain what is being done
