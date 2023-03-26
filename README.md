# Deep-Learning-Course--MIP-Warm-Start-GCNN
By Nick Masri, Sean Kelley, Michael Nardelli

### Overview

This release contains a working implementation of Neural Diving from the paper
[Solving Mixed Integer Programs Using Neural Networks](https://arxiv.org/abs/2012.13349)
with data generation built on top of that from [Exact Combinatorial Optimization
with Graph Convolutional Neural Networks](https://arxiv.org/abs/1906.01629).

The following gives a brief overview of the contents; more detailed
documentation is available within each file:

* __config_train.py__: Configuration file for training parameters.
* __data_generation.py__: Generates the feature set for each MIP instance.
* __data_utils.py__: Utility functions for feature extraction.
* __evaluate_solvers.py__: Compares solver performance between warm starts with predicted solutions and cold starts.
* __instance_generation.py__: Generates each MIP instance.
* __layer_norm.py__: Model layer normalisation and dropout utilities.
* __light_gnn.py__: The GNN model used for training.
* __sampling.py__: Sampling strategies for Neural LNS.
* __solvers.py__: Neural diving and feature generation implementation.
* __train.py__: Training script for neural diving model.
* __data__: Directory with tfrecord files to run training.

This project borrows `config_train.py`, `data_utils.py`, `layer_norm.py`,
`light_gnn.py`, `sampling.py`, and `train.py` from [Neural Local Neighborhood
Search](https://github.com/deepmind/neural_lns) and `instance_generation.py` from
[Learn2Branch](https://github.com/ds4dm/learn2branch) (respectively the implementations
for the two papers linked above). Our contributions are `data_generation.py`,
`evaluate_solvers.py`, and `solvers.py`, which form the glue code for the borrowed
files.

The above files were condensed into an .ipynb for viewing and understanding ease.

# Source
@misc{nair2020solving,
      title={Solving Mixed Integer Programs Using Neural Networks},
      author={Vinod Nair and Sergey Bartunov and Felix Gimeno and Ingrid von Glehn and Pawel Lichocki and Ivan Lobov and Brendan O'Donoghue and Nicolas Sonnerat and    Christian Tjandraatmadja and Pengming Wang and Ravichandra Addanki and Tharindi Hapuarachchi and Thomas Keck and James Keeling and Pushmeet Kohli and Ira Ktena and Yujia Li and Oriol Vinyals and Yori Zwols},
      year={2020},
      eprint={2012.13349},
      archivePrefix={arXiv},
      primaryClass={math.OC}
}

