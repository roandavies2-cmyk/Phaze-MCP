# Watch a long job

Your agent keeps an eye on a software build, 3D render, video export or any other long job on another PC. If it fails, your agent finds out why, tries to fix it, and lets you know what happened. You can carry on with your day or go to bed.

## You need

- The setup in the [README](../README.md)
- The job running, or ready to start, on the other PC
- Your agent left running, and the computer you're sitting at left awake

## The prompt

Change the parts in [brackets].

```text
Read LEARNINGS.md first, then use the Phaze MCP to connect to [PC NAME].

[APP OR COMMAND] is running [THE JOB] on that PC. If it hasn't started, start it. It's finished when [WHAT FINISHED LOOKS LIKE].

Before you start watching, tell me in a few lines what you can see: the job, its progress so far, where its log is, and where its output goes. Note the time and the progress, so you have something to compare against.

Check on it every [10] minutes. Prefer commands over the screen where you can: read the log, check the process is still running, and see whether the output is still growing. Use a screenshot when the app only shows its state on screen. Between checks, leave the PC alone.

Treat it as stuck, even with no error showing, if progress hasn't moved across [3] checks in a row. Some steps are slow, so look closely before you restart anything.

If it fails or gets stuck:
1. Save a screenshot and the relevant part of the log.
2. Find the first real error. Later errors are often caused by the first one.
3. Tell me what it says, and what you plan to change.
4. If the fix is a setting, a plugin or a restart, make the change and start the job again. Carry on from where it stopped if the app allows it, and don't overwrite finished work.
5. If the fix means changing my code or project files, deleting anything, or entering a password, don't do it. Ask me first.
6. If it fails twice with the same error, stop and wait for me.

Message me only when something fails, you change something, or it finishes. Keep it short: what happened, what you did, and whether I need to do anything.

When it finishes, check the output is really there and opens. Then tell me what failed, what you changed and how long it took, and disconnect.
```

## What helps

- **Say what finished looks like.** "The export is in this folder and plays" is easier to check than "it's done".
- **Tell your agent what it can change.** The prompt allows settings, plugins and restarts, but not your code or project files. Change that to suit you.
- **Change the check time to suit the job.** A ten hour job doesn't need checking every minute.
- **Start with a short job.** Watch your agent handle something small before you trust it overnight.
- **Keep a way back.** Use source control or a backup, so you can see and undo anything your agent changed.
