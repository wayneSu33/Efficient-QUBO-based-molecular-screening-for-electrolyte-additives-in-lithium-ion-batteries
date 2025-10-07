<h2 id="Title">Efficient QUBO-based molecular screening for electrolyte additives in lithium-ion batteriess</h2>

**Jheng-Wei Su**<sup>1*</sup>, **Zih-Chao Hong**<sup>2</sup>, **Tzu-Wei Lin**<sup>2</sup>, **Shin-Hong Liu**<sup>2</sup>, **Tsung-Hui Li**<sup>2</sup>, **Ying-Yuan Lee**<sup>2</sup>, **Ching-Ray Chang**<sup>1,3</sup>


<sup>1</sup>Department of Physics and Quantum Information Center, Chung Yuan Christian University, Taoyuan City 320314, Taiwan, R.O.C.\
<sup>2</sup>Electronics Materials Division, Formosa Plastics Corporation, Kaohsiung City 814241, Taiwan, R.O.C.\
<sup>3</sup>Graduate Institute of Applied Physics, National Taiwan University, Taipei 106319, Taiwan, R.O.C.\
<sup>\*</sup>Corresponding authors: jwsu@cycu.org.tw 

**Workflow**\
This project demonstrates a molecular screening process that combines data clustering, regression predictive model, and the QUBO model. Molecular data is clustered to enable parallelized training of the predictive model, with molecular features constructed based on fingerprints. The feature design allows the QUBO model to correspond to the predictions of the molecular properties in the predictive model through the objective function under the constraints. Subsequently, QUBO solvers are employed to screen out candidate molecules from the QUBO model. The properties of these candidates are validated using DFT, aiming to explore new potential molecules within the chemical space.
<br>

<img src="Graphical workflow.JPG" width="1000" height="600" />

<h2 id="Folders">Folders</h2> 

- **Cluster and Training**: The code file and dataset for data clustering and model training.
- **Solvers and results**: Contains code files for Fujitsu Digital Annealer (DA), exhaustive Search, simulated annealing (SA), and genetic algorithm (GA) to solve QUBO models.

<h2 id="Dependencies">Dependencies</h2>  

- Python >= 3.9.23
- pandas >= 2.3.2
- numpy >= 2.0.1
- rdkit >= 2024.3.2
- scikit-learn >= 1.6.1
- matplotlib >= 3.9.2
- pyqubo==1.5.0
- pygad==3.3.1
- dwave-neal==0.6.0
