## Train models on Physiome-ODE
To run the experiments for different models and datasets use the train_XY.py scripts provided in the experiments/training folder.
As an example we show how to run CRU on the dupont_1991b dataset for fold 0.

'''
python experiments/training/train_gruodebayes.py -dset dupont_1991b --fold 0
'''

To successfully run this you need a folder in data/IMTS_benchmark_datasets. 
All datasets contained in Physiome-ODE will be available on zenodo, after the double blind review phase
