# Persian License Plate Recognition Study Project

This repository is an archived study and integration project for detecting Persian vehicle plates, recognizing plate characters, displaying results in a desktop interface, and connecting recognized plates to simple resident or entrance records.

It assembles and adapts open-source computer-vision components, datasets, and examples. It is not presented as a production access-control product, and the repository does not currently include a maintained benchmark proving accuracy, latency, or real-time performance across deployment conditions.

## Status

- archived educational and research project;
- no active feature roadmap;
- no guaranteed support for current library, operating-system, camera, or GPU versions;
- not suitable for security-sensitive access decisions without independent testing and additional controls.

## Included Workflow

The codebase demonstrates a workflow similar to:

```text
Image or video input
    -> plate detection
    -> plate crop
    -> Persian character recognition
    -> local record lookup
    -> GUI display and event logging
```

Depending on the configured files and environment, the application may include:

- YOLOv5-based plate detection;
- a character-recognition model;
- image, video, webcam, or stream input;
- a PySide6 desktop interface;
- OpenCV-based image processing;
- local resident, permission, or entrance records.

These items describe the intended code paths, not measured production guarantees.

## Screenshots

### Main Interface

<img src="repo_images/parts.jpg" alt="Main interface with input, detected plate, recognized text, and recent entries" style="max-width:800px;">

### Resident Management

<img src="repo_images/people.jpg" alt="Resident management interface" style="max-width:800px;">

### Entrance Management

<img src="repo_images/ent.png" alt="Entrance management interface" style="max-width:800px;">

### Processing Flow

<img src="repo_images/detection_steps.png" alt="Plate detection and recognition flow" style="max-width:800px;">

## Installation

Clone this repository:

```bash
git clone https://github.com/mahdiaghtaee/persian-license-plate-recognition.git
cd persian-license-plate-recognition
```

Create an isolated Python environment and install the pinned or documented dependencies available in the repository:

```bash
python -m venv .venv
```

Activate the environment using the command appropriate for your operating system, then install dependencies:

```bash
pip install -r requirements.txt
```

Because this repository is archived, dependency versions may require adjustment for a modern environment. Review model-file locations and configuration before running the application.

## Input Configuration

The application reads its image, video, camera, or stream source from the relevant OpenCV call and configuration values used by the codebase.

Examples may include:

```python
cv2.VideoCapture(0)
```

for the default camera, or a configured file or RTSP address.

Do not place credentials for private cameras or production streams in committed configuration files.

## Run

The historical entry point is:

```bash
python home-yolo.py
```

Confirm the actual entry point, model paths, database settings, and required assets in your checkout before running it.

## Limitations

- No maintained evaluation report is included for detection accuracy, character-recognition accuracy, false positives, false negatives, or end-to-end latency.
- Performance depends on hardware, input resolution, camera angle, lighting, motion blur, plate condition, and model files.
- The repository may contain large model or research assets and is not optimized as a distributable application package.
- Authorization decisions should not rely solely on computer-vision output.
- Production deployments require authentication, audit logging, encrypted configuration, secure database access, monitoring, privacy review, retention controls, and a manual fallback process.

## Open-source Components and Data

The project was informed by and built with open-source tools and community resources, including:

- [YOLOv5](https://github.com/ultralytics/yolov5)
- [PyTorch](https://github.com/pytorch/pytorch)
- [PySide6](https://github.com/pyside/pyside-setup)
- [OpenCV](https://github.com/opencv/opencv)
- [Pillow](https://github.com/python-pillow/Pillow)

Datasets and related research resources referenced during the project include:

- [IR-LPR](https://github.com/mut-deep/IR-LPR)
- [Iranis dataset](https://github.com/alitourani/Iranis-dataset)
- [ILPR](https://github.com/amirmgh1375/iranian-license-plate-recognition)

Additional community repositories and examples may have influenced the integration approach. Review source headers, dependency licenses, dataset terms, and the repository history before redistributing models, data, or derived artifacts.

## Reproducibility

A future reproducibility update would need to add:

- exact Python and dependency versions;
- model checksums and documented model provenance;
- a small permitted evaluation dataset;
- detection and recognition metrics;
- hardware and latency measurements;
- automated tests for preprocessing, plate formatting, and database behavior;
- a clean command-line or container-based run path.

Until those items exist, treat the repository as a historical study artifact rather than a verified benchmark.

## License

This repository is distributed under the GPL-3.0 license. See [LICENSE](LICENSE).

The licenses and terms of third-party code, model weights, datasets, and research assets continue to apply independently. GPL licensing of this repository does not replace those upstream obligations.
