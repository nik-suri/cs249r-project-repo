# cs249r-project repo

## by Nikhil Suri, Thushan Puhalendran, and Samuel Clay

* [cleverhans-attacks](https://github.com/tensorflow/cleverhans): includes code referenced and used to generate
simple adversarial attacks on labeled datasets, such as MNIST. `mnist_tutorial_tf.py`
trains an MNIST classifier and shows the accuracy of the model after training and
FSGM attacks. `fast_gradient_method.py` defines the `FastGradientMethod` object,
which is an `Attack` object (defined in `attack.py`). Unfortunately, the cleverhans
attacks expect models of a specific format. It was very difficult to adapt the OpenAI
baselines agents that we trained to conform to this format.

* [cleverhans-rl-attack](https://github.com/tensorflow/cleverhans/tree/master/examples/RL-attack): includes code referenced and used in attempts to generate
adversarial attacks on OpenAI agents using cleverhans. `enjoy-adv.py` is meant to
load a pre-trained model and generate an attack for it. `train.py` can be used to
either simply train a model (which can be saved and then attack using `enjoy-adv.py`)
or attack a model during training to use adversarial training. Unfortunately, neither
of the scripts (`enjoy-adv.py` and `train.py`) worked properly.

* [openai-baselines-models](https://github.com/openai/baselines): includes weights for the Pong DQN agent that we trained
using OpenAI baselines. This agent ran successfully on OpenAI gym.

* [keras-rl](https://github.com/keras-rl/keras-rl): A copy of the keral-rl repository
with weights included for trained agents in `examples/`. Merging this with cleverhans
attacks also proved very difficult.

* [RLMA](https://github.com/RLMA2019/RLMA) RLMA code for the paper: Minimalistic Attacks: How Little it Takes to Fool a Deep Reinforcement Learning Policy, which describes methods for implementing attacks with minimal perturbation efforts

* [atari-rl](https://github.com/gsurma/atari) Alternative implemenations of OpenAI Gym RL Agents for Atari games with additional documentation, providing a source of pre-trained agents to implement and evaluate adversarial attacks on
