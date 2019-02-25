# Break-All-The-Things

I want to break things and then repair them. I expect to succeed at the first part, but maybe not the second ....

Specifically, I want to create a merge conflict.

----

## Setting up VS Code as your Git diff tool

You can set up VS code as your tool to perform merge conflicts. To do this, you set it as your **difftool** and your **mergetool** in your .gitconfig file. This can be done manually (by finding your .gitconfig file on your computer), or by running some commands in the command window/powershell.

```shell
git config --global diff.tool vscode
git config --global difftool.vscode.cmd 'code --wait --diff "$LOCAL" "$REMOTE"'
git config --global difftool.prompt false

git config --global merge.tool vscode
git config --global mergetool.vscode.cmd 'code --wait --resume "$LOCAL" "$REMOTE"'
```
