# Recommender Systems for Amazon
This is a repository for Recommender systems that has different types of item recommendation and rating prediction approaches performed on Amazon dataset.

# Algorithms

Item Recommendation:

- BPRMF

- ItemKNN

- Item Attribute KNN

- UserKNN

- User Attribute KNN

- Group-based (Clustering-based algorithm)

- Paco Recommender (Co-Clustering-based algorithm)

- Most Popular

- Random

- Content Based

Rating Prediction:

- Matrix Factorization (with and without baseline)

- Non-negative Matrix Factorization

- SVD

- SVD++

- ItemKNN

- Item Attribute KNN

- UserKNN

- User Attribute KNN

- Item NSVD1 (with and without Batch)

- User NSVD1 (with and without Batch)

- Most Popular

- Random

- gSVD++

- Item-MSMF

- (E) CoRec

Clustering:

- PaCo: EntroPy Anomalies in Co-Clustering

- k-medoids

# Evaluation and Validation Metrics

- All-but-one Protocol

- Cross-fold-Validation

- Item Recommendation: Precision, Recall, NDCG and Map

- Rating Prediction: MAE and RMSE

- Statistical Analysis (T-test and Wilcoxon)

# Requirements

- Python
- scipy
- numpy
- pandas
- scikit-learn
- GCP VM instance
- Amazon Datasets 

# Prerequisite Installations to run Notebook on GCP VM instance
Create a VM instance as shown in below article for integration of Google Colab and Google Cloud Platform. 
    - https://towardsdatascience.com/running-jupyter-notebook-in-google-cloud-platform-in-15-min-61e16da34d52

Create a firewall rule 

Update Google Cloud Platform  

    $ sudo apt-get update
    $ sudo apt-get --assume-yes upgrade
    $ sudo apt-get --assume-yes install software-properties-common

Python Package Manager and Jupyter Notebook setup on GCP 

    $ sudo apt-get install python3-pip
    $ sudo apt-get install python-setuptools python-dev build-essential
    $ sudo pip install jupyter
    $ wget http://repo.continuum.io/archive/Anaconda3-4.0.0-Linux-x86_64.sh
    $ bash Anaconda3-4.0.0-Linux-x86_64.sh (Continue Yes as default for all prompts)

Install a Python package containing Jupyter Extensions
    $ sudo apt-get install helpful_package (or)
    $ sudo pip install helpful_package
    $ jupyter serverextension enable --py helpful_package

Generate Jupyter notebook configuration file (jupyter_notebook_config.py):
    $ jupyter notebook --generate-config

Add below configuration in the Jupyter notebook config file:
    $ sudo vi ~/.jupyter/jupyter_notebook_config.py

        # Configuration file for jupyter-notebook.
        c = get_config()
        c.NotebookApp.ip = '*'
        c.NotebookApp.open_browser = False
        c.NotebookApp.port = 8089 (Note that this is TCP port configured in GCP External IP and firewall)

Launching Jupyter Notebook
    $ jupyter-notebook --no-browser --port=8089 
    
    Once console starts successfully, go to browser and run as following. Note that external ip address is the ip address which we made static and port number is the one which we allowed firewall access to as per above article. 

    http://<External Static IP Address>:<Port Number>

Download Amazon Dataset (2018) (Credits: Jianmo Ni, Jiacheng Li, Julian McAuley): 
    http://deepyeti.ucsd.edu/jianmo/amazon/index.html

    Raw review data (34gb):
    wget http://deepyeti.ucsd.edu/jianmo/amazon/categoryFiles/All_Amazon_Review.json.gz
    
    Ratings only (6.7gb):
    wget http://deepyeti.ucsd.edu/jianmo/amazon/categoryFilesSmall/all_csv_files.csv
    
    Metadata (24gb):
    wget http://deepyeti.ucsd.edu/jianmo/amazon/metaFiles/All_Amazon_Meta.json.gz
    
    Duplicated Product List (126mb):
    wget http://deepyeti.ucsd.edu/jianmo/amazon/metaFiles/duplicates.txt

# Usage

To be updated.

# Project Contribution Proecudure:

To help the project with contributions follow the steps:

- Fork recommender-sys-amazon repository

- Make your alterations and commit

- Create a branch (Tip: use your initials and feature in name - Ex: dy_matrix_vectorization) - git checkout -b dy_matrix_vectorization

- Push to your branch - git push origin dy_matrix_vectorization

- Create a Pull Request from your branch.

- This completes your contribution of changes to the project

For bugs or feedback use this link: https://github.com/deenuy/recommender-sys-amazon/issues

# Cite Us
Please feel free to use our ideas and effort, but kindly cite us in your extension. 

- Contributors: Deenu Yadav, Kaustubh Mulay, Surin Singh

# Credits
This repo is inspired from Case Recommender project: Arthur da Costa, Eduardo Fressato, Fernando Neto, Marcelo Manzato, and Ricardo Campello. 2019. Case recommender: a flexible and extensible python framework for recommender systems.

# License (MIT)

    © 2019. Case Recommender All Rights Reserved

    Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated
    documentation files (the "Software"), to deal in the Software without restriction, including without limitation the
    rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to
    permit persons to whom the Software is furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all copies or substantial portions of
    the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO
    THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
    TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS
    IN THE SOFTWARE.