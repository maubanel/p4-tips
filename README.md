# Perforce Tips

## Before You Start

* Make sure you have P4V installed (this will automatically install P4)
* Make sure that in any directory you can run `p4 -V`. You should get a response.  On a mac make sure the "p4" executable is installed inside /usr/local/bin or even /usr/bin.
* Every **Depot** needs a separate workspace.  Do not use the same workspace for multiple depots (unless just switching streams).
* Each workspace needs a unique `.p4config` file. A [batch](./files/setconfig.bat) file is available for you to use for Windows to make this easier.
* More information about the [.p4config is found here](./P4CONFIG.md).

## Commands you Need to Know
* `p4 set` (should show the content of P4Config)
* `p4 info` (shows extended info about the perforce server)
* The above two commands should show 
* Bad p4 set output:
```
P4HOST=Marcs-MacBook-Pro-2.local (enviro)
P4IGNORE=.p4ignore (enviro)
P4PORT=ssl:perforce.ncam-dt.com:16666 (enviro)
P4USER=unrealserver_background (enviro)

```
* This means that I have not set up my `.p4config` properly as the **P4HOST**, **P4PORT** and **P4USER** are wrong.

<details>
  <summary>Dev Tips &raquo;</summary>

make git m="add commit message"
</details>