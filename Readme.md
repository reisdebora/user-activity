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
jupyter labextension install jupyterlab-plotly
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

## Installing extra libraries

Install any libraries you need with

```
conda install <library>
```

Make sure to run the following command to save the installed libraries into the environment.yml file,
this allows others to run the report easily

```
conda env export --no-builds > environment.yml
```
