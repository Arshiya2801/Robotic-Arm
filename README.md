# Robotic Arm with MuJoCo

A robotics simulation project using the MuJoCo physics engine. It includes a 6-DOF robotic arm model, a quadruped model, and an arm viewer for exploring robot motion.

## Requirements

- Python 3
- Dependencies listed in `requirements.txt`

## Setup

```powershell
python -m venv mojoco_venv
.\mojoco_venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## Usage

Open the robotic arm simulation:

```powershell
python arm/arm_viewer.py
```

Record a demo video:

```powershell
python arm/arm_viewer.py --video
```

Videos are saved in the `media` folder.
