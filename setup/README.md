# Create environment

1. Crear environment a partir de archivo yml

```
cd setup
conda env create -f citt_windows.yml
conda activate citt
python -m ipykernel install --user --name citt --display-name "DUOC CITT"
```

2. Crear environment vacio y luego instalar librerias

```
conda create -n citt python=3.7
conda activate citt
conda install -y numpy matplotlib seaborn pandas ipykernel
pip install scikit-learn spacy
pip install tensorflow
pip install azureml-sdk
pip install azure-storage-blob
python -m ipykernel install --user --name citt --display-name "DUOC CITT"
```

3. Exportar el environment recientemente creado

```
conda env export > citt_windows.yml
```
