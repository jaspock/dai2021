
# Generación de HTML

## Compilación de la documentación

    conda activate dai
    cd docs
    make

or:

    conda activate dai
    cd slides
    make
    cd ../docs
    make slides
    make html
    make open

## Subir al repo

    git add newfiles
    make push

## Subir páginas estáticas

    make pages

## Instalación de miniconda

    conda=Miniconda3-latest-Linux-x86_64.sh 
    curl -O https://repo.anaconda.com/miniconda/$conda
    bash $conda

## Configuración del entorno

    conda create --name dai python=3.7.7
    conda activate dai
    conda install -c conda-forge pandoc=2.9.2.1
    python -m pip install sphinx==3.0.3 sphinx_rtd_theme==0.4.3
    conda deactivate
