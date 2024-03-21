# Evaluation of 4 new BandWidth Constrainded algorithms (BWC).

## Dependencies
* MobilityDB, PyMeos
* MovingPandas
* ...

## Data Input
The input data consists of a CSV file containing the geo-localisation of moving objects. The csv must contain at least the following columns:
* "id" : the identifier of the moving object;
* "Longitude" and "Latitude" : the coordinates;
* "Timestamp": in the format "dd/mm/yyyy hh:mm:ss".

## Usage
Compression parameters can be set in the "preprocess.py", "compress_and_evaluate.py" as well as in a ".ini" file.

Examples of ".ini" files can be found for the Bird and AIS datasets. The two files "test_10_percent.ini" and "test_30_percent.ini" contains configuration examples to compress the datasets to respectively 10 and 30 percent of their original file, for different sizes of time windods.

The data cleaning and prepossessing can be performed with:
```
python3 preprocess.py
```

The compression of the preprocessed trajectories can be performed with:
```
python3 compress_and_evaluate.py
```

## Further improvements
The algorithms are written in their individual files for isolation purposes. They 
however share many similarities and a proper OO refactoring could reduce redundancy.

# Authors
ULB
