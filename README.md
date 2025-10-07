{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "9aac840c-b327-41ec-9082-8b3b7e4287c0",
   "metadata": {},
   "source": [
    "<h2 id=\"Title\">Efficient QUBO-based molecular screening for electrolyte additives in lithium-ion batteriess</h2>\n",
    "\n",
    "**Jheng-Wei Su**<sup>1*</sup>, **Zih-Chao Hong**<sup>2</sup>, **Tzu-Wei Lin**<sup>2</sup>, **Shin-Hong Liu**<sup>2</sup>, **Tsung-Hui Li**<sup>2</sup>, **Ying-Yuan Lee**<sup>2</sup>, **Ching-Ray Chang**<sup>1,3</sup>\n",
    "\n",
    "\n",
    "<sup>1</sup>Department of Physics and Quantum Information Center, Chung Yuan Christian University, Taoyuan City 320314, Taiwan, R.O.C.\\\n",
    "<sup>2</sup>Electronics Materials Division, Formosa Plastics Corporation, Kaohsiung City 814241, Taiwan, R.O.C.\\\n",
    "<sup>3</sup>Graduate Institute of Applied Physics, National Taiwan University, Taipei 106319, Taiwan, R.O.C.\\\n",
    "<sup>\\*</sup>Corresponding authors: jwsu@cycu.org.tw \n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "39768cb5-7334-4d78-934f-9201ff2b1050",
   "metadata": {},
   "source": [
    "**Workflow**\\\n",
    "This project demonstrates a molecular screening process that combines data clustering, regression predictive model, and the QUBO model. Molecular data is clustered to enable parallelized training of the predictive model, with molecular features constructed based on fingerprints. The feature design allows the QUBO model to correspond to the predictions of the molecular properties in the predictive model through the objective function under the constraints. Subsequently, QUBO solvers are employed to screen out candidate molecules from the QUBO model. The properties of these candidates are validated using DFT, aiming to explore new potential molecules within the chemical space.\n",
    "<br>\n",
    "\n",
    "<img src=\"Graphical workflow.JPG\" width=\"1000\" height=\"600\" />\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "94861bef-5f6d-4526-b90e-20634d56ccd0",
   "metadata": {},
   "source": [
    "<h2 id=\"Folders\">Folders</h2> "
   ]
  },
  {
   "cell_type": "markdown",
   "id": "ecd7fc8e-8bee-452f-8489-6812141fbc4c",
   "metadata": {},
   "source": [
    "- **Cluster and Training**: The code file and dataset for data clustering and model training.\n",
    "- **Solvers and results**: Contains code files for Fujitsu Digital Annealer (DA), exhaustive Search, simulated annealing (SA), and genetic algorithm (GA) to solve QUBO models. "
   ]
  },
  {
   "cell_type": "markdown",
   "id": "912ef861-58b0-475c-9465-ac826213bf5b",
   "metadata": {},
   "source": [
    "<h2 id=\"Dependencies\">Dependencies</h2>  "
   ]
  },
  {
   "cell_type": "markdown",
   "id": "5f26a16e-32ac-4b46-ac33-b5e9998c7098",
   "metadata": {},
   "source": [
    "- Python >= 3.9.23\n",
    "- pandas >= 2.3.2\n",
    "- numpy >= 2.0.1\n",
    "- rdkit >= 2024.3.2\n",
    "- scikit-learn >= 1.6.1\n",
    "- matplotlib >= 3.9.2\n",
    "- pyqubo==1.5.0\n",
    "- pygad==3.3.1\n",
    "- dwave-neal==0.6.0"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.9.23"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
