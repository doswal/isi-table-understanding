# Table Understanding

### Environment Setup
Set up the environment by referring to [ISI's Table Understanding](http://github.com/usc-isi-i2/table-understanding/tree/impl/)

Once completed, few packages need to be ungraded/downgraded for the model to run
One approach is to do pip check for clashing, uncompatible package verions
Namely, the following packages will need to be installed with *stated* version respectively

- pydantic==1.74
- numpy==1.19.0
- thinc==8.0.7
- blis==0.7.11
- spacy==3.3.1
- scikit-learn==0.23.2 [to match pickle files of pre trained models, might need to use conda install instead of pip]

### JSON/Txt File Extraction:
- Kindly refer to the comments made in Jupyter Notebook attached, and generate the required .xlsx files

### PSL module, ce_model:
- Kindly download the PSL module from [this file](https://drive.google.com/file/d/1ndVTP3WSG8OLoDjYnePvuVZ5fxXBCyRz/view?usp=sharing), and ce_models from [here](https://drive.google.com/uc?id=1DJfEgqoHzfQYBllzey21zS39ui_kwId-) 
- Place the PSL Module, ce_model, data files under correct directories as in the below snapshot
{Note: /tmp/ would generate during runtime}

![alt text](https://github.com/doswal/isi-table-understanding/blob/main/data%20File%20Arrangement.png)
![alt text](https://github.com/doswal/isi-table-understanding/blob/main/tmp%20File%20Arrangement.png)
### Infersent module:
- Import or copy paste the infersent module from [here](https://github.com/facebookresearch/InferSent/blob/main/models.py) in the tabular_cell_type_classification>src>helpers.py file

### Running table-understanding pipelines
- To run a pipeline: `make run PIPELINE=<pipeline name>`
- Pipelines are defined in `./pipelines` package
- Pipelines will use `./tmp` as working directory to download model/data or generate outputs

### Check for output:
check for outputs under the /tmp/output/

### Test & Results:

As per 09/24/2024
For the given Alabama table, accurate list of blocks i.e. variables and obervation data is obtained.

For the [MD98-2177 isotopes Khider11](https://www.ncei.noaa.gov/pub/data/paleo/contributions_by_author/khider2011/khider2011.txt), the table understand runs successfully. The variables annotations are correct, however, the alignment annontations and edges for observation data do not work correctly. 

