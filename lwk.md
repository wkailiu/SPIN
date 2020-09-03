# Installation
```
conda create -n SPIN python=3.6 -y
conda activate SPIN
conda install pytorch torchvision cudatoolkit=10.1 -c pytorch
pip install -r requirements.txt
./fetch_data.sh
```

# Run Demo
```
python demo.py --checkpoint=data/model_checkpoint.pt --img=examples/im1010.jpg --openpose=examples/im1010_openpose.json
```

# conda jupyter
```
python -m ipykernel install --user --name SPIN --display-name "SPIN"
```

# Train
```
python preprocess_datasets.py --train_files

python train.py --name train_example --pretrained_checkpoint=data/model_checkpoint.pt --run_smplify
```

<!-- cdflib 代替　spacepy -->