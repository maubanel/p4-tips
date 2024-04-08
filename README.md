# Perforce Tips

* Make sure you have P4V installed (this will automatically install P4)
* Make sure that in any directory you can run `p4 -V`. You should get a response.  On a mac make sure the "p4" executable is installed inside /usr/local/bin or even /usr/bin.
* Every **Depot** needs a separate workspace.  Do not use the same workspace for multiple depots (unless just switching streams).
* Each workspace needs a unique `.p4config` file. A [batch](./files/setconfig.bat) file is available for you to use for Windows to make this easier.

<details>
  <summary>P4 Config Info</summary>
# `.p4config` does the following:
1. Creates a file called `.p4config`. This is held in your topmost root folder. This is a hidden file and hidden files must be turned on to see it
2. Adds `P4IGNORE=.p4ignore` to you config file
3. Adds **P4PORT** to the config file.  If using LSU it is: `P4PORT=ssl:helixcore.cct.lsu.edu:1818`
4. Adds `P4USER=LsuUsername` to config (do not put `@lsu.edu`
5. Adds computer host to config, `P4HOST=COMPUTERNETWORKNQME`. Mac note
6. Adds teh workspace name to the config, `P4CLIENT=WorkspaceName`
7. At the end it runs the command (does not include in the config file `p4 set P4CONFIG=.p4config`, which tells this workspace to use the `.p4config` file.
</details>

<details>
  <summary>Dev Tips &raquo;</summary>

make git m="add commit message"
</details>