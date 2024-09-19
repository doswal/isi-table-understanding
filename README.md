# Table Understanding

### Environment Setup
Set up the environment by referring to [ISI's Table Understanding](http://github.com/usc-isi-i1/table-understanding/tree/impl/)

Once completed, few packages need to be ungraded/downgraded for the model to run
One approach is to do pip check for clashing, uncompatible package verions
Namely, the following packages will need to be installed with *stated* version respectively

- pyantic==1.74
- numpy==1.22.3
- thinc==8.0.7
- blis==0.7.11
- spacy==3.3.1
- scikit-learn==0.23.2 [to match pickl files of pre trained models, might need to use conda install instead of pip]

### JSON/Txt File Extraction:
- Kindly refer to the comments made in Jupyter Notebook attached, and generate the required .xlsx files

### PSL module, ce_model:
- Kindly download the PSL module from [this file](https://drive.google.com/file/d/1ndVTP3WSG8OLoDjYnePvuVZ5fxXBCyRz/view?usp=sharing), and ce_models from [here](https://drive.google.com/uc?id=1DJfEgqoHzfQYBllzey21zS39ui_kwId-) 
- Place the PSL Module, ce_model, data files under correct directories as in the below snapshot
{Note: /tmp/ woul generate during runtime}

### Infersent module:
- Import or copy paste the infersent module from [here](https://github.com/facebookresearch/InferSent/blob/main/models.py) in the tabular_cell_type_classification>src>helpers.py file

### Running table-understanding pipelines
- To run a pipeline: `make run PIPELINE=<pipeline name>`
- Pipelines are defined in `./pipelines` package
- Pipelines will use `./tmp` as working directory to download model/data or generate outputs

### Check for output:
check for outputs under the /tmp/output/
