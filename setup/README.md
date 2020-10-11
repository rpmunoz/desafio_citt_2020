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
conda install -y numpy==1.18.5
conda install matplotlib seaborn pandas ipykernel
pip install scikit-learn spacy
pip install tensorflow==2.3.1
pip install azureml-sdk
pip install azure-storage-blob
python -m ipykernel install --user --name citt --display-name "DUOC CITT"
```

3. Exportar el environment recientemente creado

Para incluir todos los requirements y dependencias del OS
```
conda env export > citt_windows.yml
```

Para incluir solo requirements especificos, use el flag --from-history
```
conda env export --from-history > citt.yml
```
