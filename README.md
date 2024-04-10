# Perforce Tips

## Before You Start

* Make sure you have P4V installed (this will automatically install P4)
* Make sure that in any directory you can run `p4 -V`. You should get a response.  On a mac make sure the "p4" executable is installed inside /usr/local/bin or even /usr/bin.
* Every **Depot** needs a separate workspace.  Do not use the same workspace for multiple depots (unless just switching streams).
* Each workspace needs a unique `.p4config` file. A [batch](./files/setconfig.bat) file is available for you to use for Windows to make this easier.
* More information about the [.p4config is found here](./P4CONFIG.md).

## Recommended Workflow
* Every session run **P4V** and switch the desired **Workspace** and press **Get Latest**.  This means you are up to date with the head of the server. I recommend doing this in the editor and not in the game engine.
* If you are working in a game engine, before editing a level or an item save it (even if there is nothing new).  This will force the engine to check out the file.  If it saves and you don't submit it that means you can check it out and work on it.  I have too many times worked for 2 hours of a level, went to save it only to be told that it is checked out by someone else.  At that point I either have to lose all my work or have the other person lose all the their work.  The above quick save just stops that from happeing.
* Make any changes you need
* Submit either through the Game Engine or throug P4V
* When working on a game engine it is a good idea to select **Actions | Clean** in perforce before quitting your session.  This makes sure that all the files in your workspace (except for the ones being ignored) are the same version as in the depot.  If you find that your project is not identical to your teammates, you probably have filesd that are not added to the Depot.
* Double check that your Pending list is empty (all black and blue, no red folders).  Press the **Refresh** button to be sure!
* You are done with your work session.


## Commands you Need to Know
* `p4 set` (should show the content of P4Config)
* `p4 info` (shows extended info about the perforce server)
* The above two commands should show 
* Bad p4 set output. This means that I have not set up my `.p4config` properly as the **P4HOST**, **P4PORT** and **P4USER** are wrong.:
```
P4HOST=Marcs-MacBook-Pro-2.local (enviro)
P4IGNORE=.p4ignore (enviro)
P4PORT=ssl:perforce.ncam-dt.com:16666 (enviro)
P4USER=unrealserver_background (enviro)

```
* 
* Good `p4set` output:
```
output
```


## Hostnames on Mac OSX
* Mac's will change hostnames when it is on networks like LSU's with dynamic IP's (and maybe some folks home syste).
* * In **Terminal** type `hostname`.  If you see a value like `60-3e-5f-59-bf-f5.wlan.lsu.edu` then LSU is changing the hostname of your computer.  The hostname should in both Perforce and your computer should be fixed and based on your network name.
* Open **System Preference**s, click **General | Sharing** and take note of of the value in the **Local hostname** field (typically as a .local) at the end.
* Click **Edit** and make sure the "Use dynamic global hostname" checkbox is **unchecked**.
* Open up **Terminal** and check the name before the cursor and see if it i the same at the hostname above?
* If not then enter `sudo scutil --set HostName new_hostname`.  So in my case it was `sudo scutil --set HostName MarcA.local`.
* Type `hostname` in **Terminal** again and confirm that you see the correct Hostname.
<details>
  <summary>Dev Tips &raquo;</summary>

make git m="add commit message"
</details>
