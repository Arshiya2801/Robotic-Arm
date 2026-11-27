# SmolVLA Finetuning for Robotic Manipulation

Fine-tuning SmolVLA for SO-101 pick-and-place tasks, with colour and lighting augmentation to evaluate robustness under changing visual conditions.

## Project Details

- **Model:** `lerobot/smolvla_base`
- **Dataset:** `lerobot/svla_so101_pickplace`
- **Robot:** SO-101 robotic arm
- **Framework:** LeRobot
- **Task:** Pick up a cube and place it in a box.

## Approach

- Split episodes by cube position to balance training and validation data.
- Apply brightness, contrast, saturation, and hue augmentation.
- Align camera inputs and action sequences with the model.
- Evaluate predicted joint actions against recorded actions.

## Results

The reported joint-action accuracy improved from **60.92% to 87.66%** with position-balanced splitting. This measures predictions within 5% of each joint's range; it does not measure completed pick-and-place tasks.

## Usage

Run `01_train_smolvla.ipynb` to fine-tune the model, then `02_eval_offline.ipynb` to evaluate it.
