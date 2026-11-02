# Watch an Unreal build

Your agent watches an Unreal Engine project package on another PC. If the package fails, it finds out why, tries to fix it, and tells you what happened. You carry on using your own PC.

## You need

- The setup in the [README](../README.md)
- Unreal Engine and your project on the other PC
- Your agent left running, and the computer you're sitting at left awake

## The prompt

Change the parts in [brackets].

```text
Read LEARNINGS.md first, then use the Phaze MCP to connect to [PC NAME].

Open [PATH TO .UPROJECT FILE] in Unreal Engine and package it for Windows to [OUTPUT FOLDER].

Check on it every [10] minutes. Look at the Output Log and whether the packaging notification is still running.

If the package fails:
1. Find the first real error in the log. Later errors are often caused by the first one.
2. Tell me what it says, and what you plan to change.
3. If the fix is a project setting, a plugin, or a missing install, make the change and package again.
4. If the fix means changing the game's code or assets, don't change them. Ask me first.
5. If it fails twice with the same error, stop and wait for me.

When it finishes, check the packaged game is in the output folder and that it opens. Then tell me what failed, what you changed and how long it took, and disconnect.
```

## What helps

- **Have your project in source control.** You can see every change the agent made, and undo it.
- **Tell your agent what it can change.** The prompt allows settings and plugins, but not code or assets. Change that to suit you.
- **Change the check time to suit the job.** A big project doesn't need checking every minute.
- **Other builds work too.** Tell your agent how the build starts, where the log is, and what success looks like.
