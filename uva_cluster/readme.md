## Prepare dataset

```
# Install conda env
$ sbatch /home/<your-home-dir>/MoE-LLaVA/uva_cluster/install_env.job
# Download and prepare datasets
$ sbtach /home/<your-home-dir>/MoE-LLaVA/uva_cluster/prepare_datasets.job
```
## Download Eval dataset

Eval dataset is stored on a shared google drive https://drive.google.com/file/d/1atZSBBrAX54yYpxtVVW33zFvcnaHeFPy/view

```
$ pip install gdown
$ gdown --id 1atZSBBrAX54yYpxtVVW33zFvcnaHeFPy -O eval.zip
$ unzip eval.zip -d /scratch-shared/fshi/moe-llava/eval
```

Download TextVQA using instruction from https://github.com/PKU-YuanGroup/MoE-LLaVA/blob/main/docs/EVAL.md#textvqa
```
$ cd /scratch-shared/<your-user>/moe-llava/eval/textvqa/
$ wget https://dl.fbaipublicfiles.com/textvqa/data/TextVQA_0.5.1_val.json
$ wget https://dl.fbaipublicfiles.com/textvqa/images/train_val_images.zip
# unzip train_val_images.zip
```

## Run Eval