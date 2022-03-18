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

```bash
pdc source builds && open builds/source.pdx/
```
