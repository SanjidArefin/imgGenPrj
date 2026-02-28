# imgGenPrj

`imgGenPrj` is a hybrid video frame generation and interpolation project.
It combines a pre-trained image generator with algorithm-based frame interpolation.
An SSIM feedback loop is used to improve frame consistency, semantic alignment, and visual coherence.

## Project Goals

- Build a practical video interpolator for 2D and 3D animation workflows.
- Reduce compute cost while keeping frame quality and consistency high.

## Achievements

- About 45% lower cost.
- About 26% lower resource usage.
- Improved frame-to-frame consistency using SSIM-guided optimization.

## Future Work

- Build a user-friendly interface for easier adoption and commercial use.

## Setup Notes

- Place model files such as `flownet.pkl` and `IFNet_HDv3` in `path\to\train_log`.
- Put your input video (for example, `file1.mp4`) in the expected project folder.
- Update script input settings in `inference_video.py` if your local paths differ.

## How It Works (Step by Step)

- The system takes a video input path (for example, `path\to\folder\file1.mp4`) through script arguments.
- A pre-trained model generates a key frame with strong semantic quality.
- The interpolation module generates intermediate frames using algorithm-based frame prediction.
- SSIM is used in a quality loop to compare generated frames and improve consistency.
- The pipeline outputs a refined sequence of frames or an interpolated video stream.

## What To Expect After Running

### Successful execution

- The script loads required model files and reads the input video correctly.
- Intermediate frames are generated with smoother transitions.
- Output is produced with better visual coherence across adjacent frames.
- You should see improved consistency compared to basic interpolation-only output.

### Unsuccessful execution

- Missing model files in `path\to\train_log`.
- Wrong input path, unsupported file, or unreadable video.
- Runtime errors from dependency mismatch or script configuration issues.

### What to do if execution is unsuccessful

- Verify model files are present in the expected folder and names are correct.
- Confirm your input video path is valid (for example, `path\to\folder\file1.mp4`).
- Re-check script arguments and dependency versions, then run again.

## Validation Rules

- Input video path must exist and be readable before processing starts.
- Required model files must be available before inference runs.

## Conflict Handling

- If an output name already exists, create a new filename using suffixes like `(1)`, `(2)`, and so on.

## Failure Scenarios

- Model weights are missing or placed in the wrong folder.
- Input video is corrupted or not in a supported format.
- Inference stops due to incorrect environment or dependency versions.

## User Recovery Steps

- Re-download and place all required model files in the correct directory.
- Test with a small known-good video file (for example, `file1.mp4`).
- Reinstall or align package versions, then rerun the pipeline.
