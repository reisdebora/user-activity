# Exploring and plotting data from Mongodb

## Installation

Git clone this repository:

```
git clone https://github.com/kyso-io/template
```

Download and install the [Anaconda Python distribution](https://www.anaconda.com/distribution/).
Then active a conda virtual environment with

```
conda env create -f environment.yml
conda activate dev

```

## Usage

Make sure to define your Mongo connection url with

```
export MONGO_CONNECTION_URL="YOUR_CONNECTION_STRING"
```

Start programming! Open jupyter with

```
jupyter lab
```

And start working.

## Sharing

Push to Github and import into Kyso.

If you have big files (bigger than 100MB), you should also install GIT LFS to store them at Git repository:

```
brew install git-lfs
git lfs install
git lfs install --system
git lfs track '*.csv'
git lfs track '*.json'
```

## Installing extra libraries

Install any libraries you need with

```
conda install <library>
```

Make sure to run the following command to save the installed libraries into the environment.yml file,
this allows others to run the report easily

```
conda env export --no-builds > environment.yml
conda activate dev
python -m pip install plotly
jupyter labextension uninstall @jupyterlab/plotly-extension
jupyter labextension install jupyterlab-plotly
python -m pip install cufflinks
python -m pip install psutil
python -m pip install statsmodels 
```

## MongoDB Connection

You have to make sure that you have MongoDB installed in your computer. If not, install it in command line with:
```
brew install mongodb-community
brew services start mongodb-community
python -m pip install pymongo
```

Look at your MongoDB connection URI. If your connection begins with "mongodb+srv:" you need to make sure to install dnspython with: 

```
python -m pip install dnspython
```

If you use MongoDB Atlas, you can find some steps to find your URI at https://docs.atlas.mongodb.com/driver-connection/.