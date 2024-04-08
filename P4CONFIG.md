# P4 Config Info

`.p4config` does the following:<br>
1. Creates a file called `.p4config`. This is held in your topmost root folder. This is a hidden file and hidden files must be turned on to see it.<br><br>
3. Adds `P4IGNORE=.p4ignore` to you config file.<br><br>
3. Adds **P4PORT** to the config file.  If using LSU it is: `P4PORT=ssl:helixcore.cct.lsu.edu:1818`.<br><br>
4. Adds `P4USER=LsuUsername` to config (do not put `@lsu.edu`.<br><br>
5. Adds computer host to config, `P4HOST=COMPUTERNETWORKNQME`. Mac note.<br><br>
6. Adds the workspace name to the config, `P4CLIENT=WorkspaceName`.<br><br>
7. At the end it runs the command (does not include in the config file `p4 set P4CONFIG=.p4config`, which tells this workspace to use the `.p4config` file.<br>

#Sample Content to .p4cong:

```
P4IGNORE=.p4ignore
P4PORT=ssl:helixcore.cct.lsu.edu:1818
P4USER=maubanel
P4HOST=ComputerName
P4CLIENT=WorkspaceName
```
