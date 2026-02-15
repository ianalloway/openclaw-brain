# ai-drone-auto-vehicle

## Overview

Autonomous vehicle intelligence platform with YOLOv8 vision, A*/RRT* path planning, behavior trees, and MAVLink integration.

**Location:** `https://github.com/ianalloway/ai-drone-auto-vehicle`
**Status:** Active

## Tech Stack

- **Language:** Python 3.x
- **Vision:** YOLOv8 (ultralytics), OpenCV, PyTorch
- **Path Planning:** A*, RRT*, NetworkX, SciPy
- **Drone Comm:** pymavlink, dronekit
- **Sensors:** Kalman filters (filterpy)
- **Config:** YAML, python-dotenv
- **Logging:** loguru
- **Testing:** pytest, pytest-asyncio

## Folder Structure

```
ai-drone-auto-vehicle/
├── config/           # Configuration files
├── examples/         # Example scripts
├── src/
│   ├── sensors/      # Sensor processing
│   ├── planning/     # Path planning (A*, RRT*)
│   ├── vision/       # YOLOv8 vision
│   ├── decision/    # Behavior trees
│   └── communication/ # MAVLink
├── requirements.txt
└── README.md
```

## Key Dependencies

```
numpy>=1.24.0
opencv-python>=4.8.0
torch>=2.0.0
ultralytics>=8.0.0
networkx>=3.0
pymavlink>=2.4.0
dronekit>=2.9.2
filterpy>=1.4.5
```

## Entry Points

- Main scripts in `src/` directories
- Config in `config/`
- Examples in `examples/`

## Stability

- Core path planning is stable
- Vision module well-tested
- Drone communication may need hardware-specific tuning

## Notes

- No secrets required
- Can modify everything
- Built with Devin assistance
