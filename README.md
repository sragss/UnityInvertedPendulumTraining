# UnityInvertedPendulumTraining

## Dependency setup
* Create a venv for the project: `python3 -m venv ~/python-envs/robot-spin-env`
* Activate: `source ~/python-envs/robot-spin-env/bin/activate`
* Install ML-Agents: `pip3 install mlagents`

## Run training
`mlagents-learn config/trainer_config.yaml --run-id="<somerunid>"`

## Run inferenece
* `mlagents-learn config/trainer_config.yaml --run-id="<somerunid>" --inference`
* Not really a point to doing this over just running with a brain in the editor itself.

## Run training with curriculum
`mlagents-learn config/trainer_config.yaml --run-id="<somerunid>" -train --curriculum=config/curriculum.yaml`

## View results in tensorboard
* `tensorboard --logdir=summaries`
* Navigate to localhost:6006


## Debugging
* For incompatability between apis (message like "The communication API version is not compatible between Unity and python") try checking out the latest branch of ML-Agents then reinstalling with:
    * `cd ml-agents-envs && pip install -e . && cd ../ml-agents && pip install -e .`
    * Then you may have to relaunch your venv to see the changes

## Other notes
* Not sure if ml-agents and ml-agents-envs are required, but gave up on debugging.