# ComfyUI Jason Node
Some Custom Node I made for comfyui

# SDXLMixSampler
The concept is to make one node to use both base+refiner like simple sampler.
Let me explains some parameter.
total_steps: total steps would run with this sampler. default is 20.
mixing_steps: total steps of one loop, loop = total_steps / mixing steps
base_steps_percentage: the percentage of base model's steps in each loop, the refiner would take the leftover

The whole pocess would only add_noise at the first base model sampling, other would disable_noise.
The return_with_leftover_noise would be false at the last refiner node.

While would I create this node?
I was testing around generating text and I found it helps to generating text in multiple loop of the base+refiner process
and I think it could done by 1 node.
