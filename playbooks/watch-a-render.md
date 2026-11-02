# Watch a render

Your agent starts a Blender render on another PC, checks on it, restarts it if it stops, and tells you what happened. You carry on using your own PC.

## You need

- The setup in the [README](../README.md)
- Blender and your project on the other PC
- Your agent left running, and the computer you're sitting at left awake

## The prompt

Change the parts in [brackets].

```text
Read LEARNINGS.md first, then use the Phaze MCP to connect to [PC NAME].

Open [PATH TO .BLEND FILE] in Blender and render the animation.

Before you start:
- Make sure the output is an image sequence going to [OUTPUT FOLDER], not a video file.
- Turn Overwrite off in Output Properties, so finished frames are kept if we restart.
- Don't change anything else in the scene.
- Tell me the frame range and how many frames are already in the folder.

Start the render, then check on it every [10] minutes:
- Look at the frame counter, and count the files in the output folder.
- If the count hasn't moved since the last check, take a closer look.

If the render has stopped or Blender has crashed:
1. Save a screenshot of any error, and tell me what it says.
2. Open the same file and start the render again. Overwrite being off means it carries on from the frames it hasn't done.
3. If it stops twice on the same frame, don't keep trying. Tell me which frame it is and wait for me.

When it finishes, check that every frame in the range is in the folder, tell me the total time, then disconnect.
```

## What helps

- **Use an image sequence.** A restart can skip finished frames, which a video file can't do.
- **Change the check time to suit the job.** A slow render doesn't need checking every minute.
- **Other render apps work too.** Tell your agent where the progress shows and what a restart looks like in that app.
