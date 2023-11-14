## Experiment Replication of Process Prediction Models using Attention Mechanisms
This directory contains code used to replicate the following study:

`Building Interpretable Models for Business Process Prediction using Shared and Specialised Attention Mechanisms`, 
by Bemali Wickramanayakea, Zhipeng Hea, Chun Ouyanga, Catarina Moreiraa, Yue Xua, and Renuka Sindhgatta

(
  @article{wickramanayake2022building,
    title={Building interpretable models for business process prediction using shared and specialised attention mechanisms},
    author={Wickramanayake, Bemali and He, Zhipeng and Ouyang, Chun and Moreira, Catarina and Xu, Yue and Sindhgatta, Renuka},
    journal={Knowledge-Based Systems},
    volume={248},
    pages={108773},
    year={2022},
    publisher={Elsevier}
  }
)

The following prerequisites are to be downloaded in order to run the notebooks:

- Jupyter Lab
- TensorFlow>=2.5
- pandas
- scipy
- numpy
- seaborn
- pyflowchart
- plotly


### Model Performance
The performance measures obtained for component (i) of the experiments (see report) are obtained using 5 similar notebooks. These notebooks can simply be run from top to bottom using Jupyter Notebook, or by first pressing 'Kernel' in the toolbar, and choosing 'Restart & Run All' subsequently. This will conduct the 5 repetitions of component (i) of the experiments, and show the average performance measures of the shared and specialised attention models in separate dataframes. The experiment repetitions are divided into notebooks based on the event log the models are run on. These logs (and corresponding notebooks) are the following:

- BPIC 2012 Complete -- `bpic_2012_all.ipynb`
- BPIC 2012 A -- `bpic_2012_A.ipynb`
- BPIC 2012 O -- `bpic_2012_O.ipynb`
- BPIC 2012 W Complete -- `bpic_2012_W.ipynb`
- BPIC 2017 Complete -- `bpic_2017_all.ipynb`

Note that the experiments can be conducted with or without data shuffling during data pre-processing. This can be modified manually in the notebook in the cell underneath markdown cell `Replicate Experiments`, in lines 23 and 26 (explained how this can be done in the comment in line 22). Also, note that the accuracies obtained in this notebook are the same accuracies as used for component (ii) of the experiments, like in the original paper. 

### Decision Point Analysis
The performance measures obtained for component (iii) of the experiments (see report) are obtained using 2 similar notebooks. These notebooks can simply be run from top to bottom using Jupyter Notebook, or by first pressing 'Kernel' in the toolbar, and choosing 'Restart & Run All' subsequently. This will show the global and local explanations extracted from the shared and specialised models, with which component (iii) of the original paper is replicated. The notebooks with which these results are obtained are the following:

- Decision Point "A_PREACCEPTED" -- `bpic_2012_A_PREACCEPTED.ipynb`
- Decision Point "W_Nabellen offertes" -- `bpic_2012_W_Nabellen offertes.ipynb`

Note that the final parameter of the (shared_)explain_local function denotes the particular case for which a prediction was made. Modifying this parameter results in different extractions for different predictions.

