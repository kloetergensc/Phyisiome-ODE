# Physiome-ODE
This is the Git Repository from 
	
Physiome-ODE: A Benchmark for Irregularly Sampled Multivariate Time-Series Forecasting based on ODEs,
submitted to the Thirteenth International Conference on Learning Representations (ICLR 2025)

Current Leaderboard, subject to updates:

| Dataset   |        JGD | IMTS-Mixer       | GRU-ODE-Bayes   | LinODENet        | CRU              | Neural Flows   | GraFITi          | GraFITi-C        |
|:----------|-----------:|:-----------------|:----------------|:-----------------|:-----------------|:---------------|:-----------------|:-----------------|
| DUP01     | 2.69704    | 0.958± 0.038     | 1.037± 0.047    | 0.964± 0.036     | 0.958± 0.038     | 1.030± 0.046   | 0.955± 0.037     | **0.951± 0.036** |
| JEL01     | 2.57955    | 0.946± 0.018     | 1.017± 0.014    | 0.949± 0.015     | 0.939± 0.015     | 1.000± 0.013   | 0.942± 0.020     | **0.935± 0.016** |
| DOK01     | 2.27746    | **0.980± 0.005** | 1.011± 0.004    | 0.996± 0.003     | 0.985± 0.005     | 0.998± 0.005   | 0.984± 0.005     | 0.982± 0.005     |
| INA01     | 2.21773    | **1.004± 0.009** | 1.018± 0.010    | 1.009± 0.011     | 1.005± 0.010     | 1.008± 0.008   | **1.004± 0.010** | **1.004± 0.009** |
| WOL01     | 1.97251    | 0.799± 0.030     | 0.952± 0.035    | 0.806± 0.027     | 0.814± 0.029     | 0.841± 0.029   | 0.787± 0.028     | **0.784± 0.030** |
| BOR01     | 1.7947     | 0.715± 0.022     | 0.794± 0.034    | 0.719± 0.021     | 0.715± 0.020     | 0.743± 0.026   | 0.712± 0.022     | **0.709± 0.022** |
| HYN01     | 1.54821    | 0.625± 0.050     | 0.883± 0.060    | 0.672± 0.044     | 0.665± 0.053     | 0.636± 0.045   | 0.625± 0.043     | **0.619± 0.046** |
| JEL02     | 1.27073    | 0.691± 0.032     | 0.816± 0.049    | 0.693± 0.031     | **0.674± 0.028** | 0.779± 0.028   | 0.699± 0.029     | 0.687± 0.027     |
| DUP02     | 1.20166    | 0.728± 0.045     | 0.895± 0.055    | 0.740± 0.042     | 0.722± 0.046     | 0.890± 0.081   | 0.728± 0.044     | **0.718± 0.046** |
| WOL02     | 0.89486    | 0.649± 0.017     | 0.854± 0.010    | 0.663± 0.015     | 0.653± 0.017     | 0.685± 0.012   | 0.654± 0.014     | **0.645± 0.016** |
| DIF01     | 0.734917   | 0.966± 0.026     | 1.035± 0.023    | **0.832± 0.087** | 0.985± 0.025     | 1.014± 0.025   | 0.985± 0.030     | 0.982± 0.029     |
| VAN01     | 0.40662    | 0.245± 0.005     | 0.321± 0.023    | 0.250± 0.006     | 0.253± 0.005     | 0.250± 0.006   | 0.246± 0.005     | **0.242± 0.006** |
| DUP03     | 0.253855   | **0.619± 0.049** | 0.874± 0.089    | 0.632± 0.044     | 0.622± 0.047     | 1.098± 0.447   | 0.627± 0.043     | 0.744± 0.042     |
| BER01     | 0.178554   | **0.279± 0.016** | 0.594± 0.054    | **0.279± 0.020** | 0.280± 0.016     | 0.398± 0.014   | 0.300± 0.018     | 0.342± 0.018     |
| LEN01     | 0.178223   | 0.688± 0.043     | 1.028± 0.060    | **0.387± 0.071** | 0.754± 0.157     | 1.009± 0.061   | 0.607± 0.055     | 0.970± 0.063     |
| LI01      | 0.112681   | 0.262± 0.074     | 1.067± 0.015    | **0.084± 0.009** | 0.175± 0.020     | 0.979± 0.049   | 0.202± 0.013     | 0.742± 0.010     |
| LI02      | 0.0974261  | **0.388± 0.046** | 0.723± 0.080    | 0.434± 0.044     | 0.437± 0.046     | 0.674± 0.105   | 0.397± 0.058     | 0.458± 0.056     |
| REV01     | 0.0812904  | 0.631± 0.052     | 1.091± 0.075    | **0.597± 0.061** | 0.602± 0.049     | 0.978± 0.042   | 0.674± 0.055     | 0.855± 0.050     |
| PUR01     | 0.0485329  | 0.158± 0.013     | 0.703± 0.058    | **0.106± 0.006** | 0.353± 0.083     | 0.654± 0.102   | 0.153± 0.006     | 0.476± 0.020     |
| NYG01     | 0.0465165  | **0.269± 0.062** | 0.571± 0.074    | 0.358± 0.071     | 0.403± 0.092     | 0.442± 0.094   | 0.344± 0.065     | 0.366± 0.047     |
| PUR02     | 0.0437351  | **0.273± 0.016** | 0.830± 0.066    | 0.280± 0.028     | 0.293± 0.026     | 0.723± 0.077   | 0.322± 0.021     | 0.511± 0.023     |
| HOD01     | 0.0420774  | **0.399± 0.039** | 0.851± 0.118    | 0.441± 0.043     | 0.409± 0.049     | 0.701± 0.077   | 0.493± 0.046     | 0.609± 0.056     |
| REE01     | 0.034614   | 0.045± 0.018     | 0.266± 0.068    | 0.045± 0.012     | 0.051± 0.008     | 0.045± 0.011   | **0.033± 0.007** | 0.039± 0.012     |
| VIL01     | 0.0284104  | **0.322± 0.029** | 0.511± 0.053    | 0.374± 0.021     | 0.373± 0.039     | 0.500± 0.060   | 0.344± 0.044     | 0.378± 0.042     |
| KAR01     | 0.0229884  | **0.032± 0.012** | 0.193± 0.013    | 0.034± 0.008     | 0.044± 0.012     | 0.069± 0.009   | 0.041± 0.013     | 0.078± 0.011     |
| SHO01     | 0.0225755  | 0.058± 0.014     | 0.260± 0.017    | 0.057± 0.006     | 0.095± 0.010     | 0.092± 0.014   | 0.062± 0.013     | **0.055± 0.013** |
| BUT01     | 0.0197068  | **0.203± 0.041** | 0.583± 0.172    | 0.254± 0.074     | 0.317± 0.108     | 0.441± 0.153   | 0.281± 0.071     | 0.324± 0.091     |
| MAL01     | 0.0190455  | **0.015± 0.003** | 0.420± 0.061    | 0.018± 0.007     | 0.064± 0.007     | 0.052± 0.002   | 0.020± 0.004     | 0.054± 0.005     |
| ASL01     | 0.0188896  | **0.012± 0.001** | 0.114± 0.035    | 0.022± 0.003     | 0.046± 0.014     | 0.066± 0.033   | 0.025± 0.009     | 0.026± 0.002     |
| BUT02     | 0.016367   | **0.179± 0.025** | 0.483± 0.047    | 0.207± 0.056     | 0.282± 0.042     | 0.329± 0.068   | 0.248± 0.052     | 0.256± 0.039     |
| MIT01     | 0.0153166  | **0.003± 0.000** | 0.005± 0.001    | **0.003± 0.000** | **0.003± 0.000** | 0.008± 0.004   | **0.003± 0.000** | **0.003± 0.000** |
| GUP01     | 0.0141431  | **0.012± 0.005** | 0.153± 0.041    | 0.018± 0.007     | 0.057± 0.017     | 0.043± 0.017   | 0.041± 0.006     | 0.035± 0.006     |
| GUY01     | 0.0132988  | **0.004± 0.001** | 0.036± 0.004    | 0.006± 0.005     | **0.004± 0.001** | 0.024± 0.015   | 0.005± 0.003     | **0.004± 0.001** |
| PHI01     | 0.0132527  | 0.133± 0.023     | 0.674± 0.030    | **0.131± 0.014** | 0.133± 0.020     | 0.635± 0.158   | 0.222± 0.013     | 0.345± 0.015     |
| GUY02     | 0.0130711  | **0.008± 0.002** | 0.124± 0.044    | 0.010± 0.006     | 0.010± 0.002     | 0.082± 0.066   | 0.012± 0.009     | 0.032± 0.015     |
| PUL01     | 0.0129311  | **0.006± 0.002** | 0.099± 0.024    | 0.008± 0.004     | 0.012± 0.003     | 0.061± 0.060   | 0.008± 0.001     | 0.024± 0.008     |
| CAL01     | 0.0129047  | 0.094± 0.011     | 1.049± 0.055    | **0.078± 0.009** | 0.158± 0.008     | 0.867± 0.014   | 0.179± 0.012     | 0.643± 0.024     |
| WOD01     | 0.0122696  | 0.131± 0.019     | 0.612± 0.072    | 0.154± 0.016     | **0.113± 0.017** | 0.510± 0.060   | 0.164± 0.013     | 0.344± 0.016     |
| GUP02     | 0.0122064  | **0.429± 0.022** | 0.870± 0.059    | 0.469± 0.022     | 0.444± 0.018     | 0.577± 0.017   | 0.449± 0.027     | 0.461± 0.025     |
| M01       | 0.0120677  | **0.003± 0.000** | 0.055± 0.009    | 0.004± 0.001     | 0.005± 0.000     | 0.124± 0.207   | **0.003± 0.000** | **0.003± 0.000** |
| LEN02     | 0.0120132  | 0.042± 0.008     | 0.297± 0.071    | **0.039± 0.005** | 0.059± 0.012     | 0.380± 0.141   | 0.099± 0.021     | 0.143± 0.022     |
| KAR02     | 0.0111432  | 0.154± 0.007     | 0.515± 0.032    | **0.140± 0.010** | 0.151± 0.011     | 0.257± 0.016   | 0.151± 0.009     | 0.252± 0.010     |
| SHO02     | 0.0108923  | **0.026± 0.004** | 0.368± 0.028    | 0.037± 0.006     | 0.083± 0.015     | 0.109± 0.015   | 0.043± 0.006     | 0.073± 0.010     |
| MAC01     | 0.00993406 | **0.016± 0.002** | 0.242± 0.026    | 0.020± 0.003     | 0.065± 0.006     | 0.029± 0.011   | 0.021± 0.003     | 0.019± 0.002     |
| IRI01     | 0.00983166 | **0.031± 0.004** | 0.151± 0.032    | 0.037± 0.003     | 0.049± 0.010     | 0.116± 0.006   | 0.038± 0.017     | 0.097± 0.008     |
| BAG01     | 0.00979835 | **0.028± 0.002** | 0.294± 0.041    | 0.032± 0.005     | 0.046± 0.005     | 0.075± 0.012   | 0.029± 0.002     | 0.109± 0.002     |
| WOL03     | 0.00844305 | 0.079± 0.011     | 0.859± 0.114    | **0.073± 0.010** | 0.177± 0.016     | 0.479± 0.107   | 0.105± 0.016     | 0.247± 0.032     |
| WAN01     | 0.00804384 | 0.104± 0.005     | 0.504± 0.031    | **0.103± 0.012** | 0.125± 0.012     | 0.345± 0.027   | 0.119± 0.010     | 0.232± 0.015     |
| NEL01     | 0.00730373 | **0.007± 0.001** | 0.054± 0.012    | 0.010± 0.001     | 0.009± 0.001     | 0.060± 0.029   | **0.007± 0.000** | 0.023± 0.006     |
| HUA01     | 0.00670105 | **0.044± 0.004** | 0.321± 0.046    | 0.052± 0.004     | 0.116± 0.007     | 0.149± 0.015   | 0.063± 0.005     | 0.115± 0.007     |


# Requirements
We recommend to create a fresh environment on Python 3.13
```bat
conda create -n physiome python==3.13 
```
```bat
conda activate physiome
```
```bat
pip install -r requirements.txt 
```

# Downloading the dataset

Physiome-ODE can be downloaded on Zenodo: https://zenodo.org/records/11492058

# Recreating or modifying the dataset (Optional)
Instead of downloading our version of Physiome-ODE you can also create your own version with any desired modification. 
For that we shared a detailed step-by-step instruction in the data_creation/README.md. 

# Train models on Physiome-ODE
To run the experiments for different models and datasets use the train_XY.py scripts provided in the experiments/training folder.
As an example we show how to run CRU on the dupont_1991b dataset for fold 0.

```bat
cd  experiments/training
```

```bat
python train_gruodebayes.py -dset dupont_1991b --fold 0
```

To successfully run this you need a folder named dupont_1991b in data/final/. 

# Adding new models to the benchmark. 

Adding new models to Physiome-ODE is simple. We recommend implementing a new model in the training/models folder.
Furthermore, you might consider implementing a custom collate function tailored for your model to map the format 
of the IMTS data from our format to the format that your model. 
As an example see experiments/training/models/train_linodenet.py and its respective
collate function in experiments/training/models/linodenet/utils/data_utils.py

We are open to add new published models to the repo that can be contributed by the community. 
