# UnityInvertedPendulumTraining

## Dependency setup
* Create a venv for the project: `python3 -m venv ~/python-envs/robot-spin-env`
* Activate: `source ~/python-envs/robot-spin-env/bin/activate`
* Install ML-Agents: `pip3 install mlagents`

## Run training
`mlagents-learn config/trainer_config.yaml --run-id="<somerunid>" --train`

## Run training with curriculum
`mlagents-learn config/trainer_config.yaml --run-id="<somerunid>" -train --curriculum=config/curriculum.yaml`

## View results in tensorboard
* `tensorboard --logdir=summaries`
* Navigate to localhost:6006