# buzzle-action-video-orientation for Nexrenderer

Module for changing orientaion of your encoded video

# Action: Change Video Orientation

Change Video Orientation of your encoded video,
You don't need to have ffmpeg installed on your system.

## Installation

If you are using [binary](https://github.com/inlife/nexrender/releases) version of the nexrender,
there is no need to install the module, it is **included** in the binary build.

<!-- ```
npm i action-watermark -g
``` -->

## Usage

When creating your render job provide this module as one of the `postrender` actions:

```json
// job.json
{
  "actions": {
    "postrender": [
      {
        "module": "buzzle-action-video-orientation",
        "input": "landscpae.mp4",
       "transpose": 1,
        "orientaion": "portrait",
        "output": "outputWithChangedOrientation.mp4"
      }
    ]
  }
}
```

## Information

- `output` is a path on your system where result will be saved to, can be either relative or absoulte path.
- `input` path of the video file you want to add video to, can be either relative or abosulte path. Defaults to current job output video file.
- `orientaion` is the orientaion of output video, value will be `landscape` or `portrait`.
- `transpose` is the enum for rotating video  
```
 0 = 90CounterCLockwise and Vertical Flip (default)
 1 = 90Clockwise
 2 = 90CounterClockwise
 3 = 90Clockwise and Vertical Flip
```
