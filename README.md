# spikeflow

Spiking neural networks in tensorflow.

**Hypothesis:** Biological plausibility in neural networks is not an obstacle, but a benefit, for machine learning applications.

**Proof:** None. Yet.

The purpose of this library is to explore the connection between computational neuroscience and machine learning, and to practice implementing efficient and fast models in tensorflow.

Spikeflow makes it easy to create arbitrarily connected layers of spiking neurons, and thence to 'step time'.

Spikeflow will concentrate on facilitating the exploration of spiking neuron models, local-only learning rules, dynamic network construction, and the role of inhibition in the control of attractor dynamics.

Spikeflow will implement:
- multiple models of spiking neurons, including
  - Leaky Integrate-and-fire
  - Izhikevich
  - Hodgkin-Huxley
- arbitrary connections between layers of similar neurons, including feed-foward, recurrent, skip connections, and inhibition.
- multiple models of synapses, including
  - simple weights
  - decay synapses
  - delay synapses
- out-of-graph and in-graph learning rules, including
  - simple hebbian synaptic modification
  - symmetric and asymmetric STDP
- forms of dynamic neural network construction, including
  - Synaptic pruning and synaptogenesis
  - Neuron pruning and neurogenesis
  - Other structure modification

The basic modelling idea is this:

```
model = BPNNModel(input_shape,
  [ neuronlayer1, neuronlayer2, ...],
  [ connections1, connections2, ...])

model.run_time(data_generator, end_time_step_callback)
```

See the examples in the `jupyter_examples` directory.

Feedback and collaborators welcome!
