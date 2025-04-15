# MSGAT: Metapath-based Syncrhonized Graph Attention Network

# MCGAT
We developed a Metapath-based Synchronized Graph Attention Network(MSGAT) for herb-disease association prediction.
We applied a novel 'Cross-type synchronization' mechanism and 'Incremental metapath optimization' in MSGAT.

## Requirements
Python version
* `python` == 3.11.5


## Required packages
* `pandas` == 2.0.3
* `numpy` == 1.24.3
* `torch` == 2.1.2+cu121
* `dgl` == 2.0.0+cu121


## Required input files
Input files need to run the codes. These files should be in the `data` folder.

* `coconut_he_cp.csv` - The relationships between herb and compound from COCONUT

* `coconut_he_ph.csv` - The relationships between herb and phenotype from COCONUT

* `cp_cp_id.csv` - The relationships between compound and compound from CODA

* `cp_ph_id.csv` - The relationships between compound and phenotype from CODA

* `ph_ph_id.csv` - The relationships between phenotype and phenotype from CODA

## Run analysis
Run `main.py` for model training and testing.
If you want to select metapaths with incremental metapath optimization, run `incremental_metapath_optimization.py` several times and select metapaths with the highest performance.

## Model performance
|  | **KNN** | **LR** | **MLP** | **GB** | **GCN** | **GAT** | **HAN** | ***MCGAT*** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **AUROC** | 0.6208 | 0.6762 | 0.6500 | 0.6940 | 0.7361 | 0.7447 | 0.7536 | **0.7586** |
| **AUPRC** | 0.6305 | 0.6755 | 0.6223 | 0.6967 | 0.7144 | 0.7116 | 0.7132 | **0.7240** |

![image](https://github.com/user-attachments/assets/a5490264-1867-486f-98d8-f481821b5d98)


![image](https://github.com/user-attachments/assets/fa67873d-60e2-42f0-a110-816fd90280ce)

