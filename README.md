# Sources

I adapted this repository from this [original template Playdate project](https://github.com/Whitebrim/VSCode-PlaydateTemplate).

I followed (mostly, apart from Windows specific set up stuff) this [video tutorial](https://www.youtube.com/watch?v=AY9MnQ4x3zk) to get up to speed on the Playdate SDK basics.

# Instructions

This repo was originally made for building on Windows.

I've adjusted these instructions to work for my CLI preference MacOS setup:

1. Download and install the Playdate SDK: [https://play.date/dev/](https://play.date/dev/)
2. Export a `PLAYDATE_SDK_PATH` environment variable pointing to your Playdate SDK. I added this line to my `.bash_profile` to do this.
   ```bash
   export PLAYDATE_SDK_PATH="/Users/rkubik/Developer/PlaydateSDK"
   ```
3. To build, run:
   ```bash
   pdc source builds
   ```
   This creates a build from the source directory in the `builds` directory. The new build is a directory with a `.pdx` extension. It's executable on MacOS when viewed from Finder. Launching it runs the Playdate simulator version.
4. You can use the `open` command to launch the simulator from the command line:
   ```bash
   open builds/source.pdx/
   ```

This command combines the two above to quickly rebuild and relaunch the playdate simulator after a change.

```bash
pdc source builds && open builds/source.pdx/
```
