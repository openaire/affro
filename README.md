# Matching Repository

This repository contains code and data for matching DOIs of crossref JSON files with organization IDs from the OpenAIRE database.

## Files

- `matching.py`: This is the main code for the matching process. It takes JSON files as input and returns a JSON (`output.json`) with matchings between the DOIs of the JSONs and IDs of organizations in the OpenAIRE database. 
The organizations include universities, institutions, hospitals, labs.

- `matching.ipynb`: Is a Jupyter Notebook for testing the code. In addition to the JSON file (`output.json`) it returns two EXCEL files (`affilMatch` and `doisMatch` respectively), one with the distinct affiliations of the JSON input, the matched openAIRE organizations and the corresponding similarity scores and one with the DOIs of the JSON input and the matched openAIRE organizations and the similarity scores.

- `dixAcadRor.pkl`: This file is a pickled dictionary that contains keys representing legalnames and alternativenames of organizations in the OpenAIRE database. 
The corresponding values are the ROR PIDs (Persistent Identifiers) associated with each organization.
Note: the prefix of the openAIRE id of all organizations considered is `openorgs_`.

- `sample.json`: Is a sample of 1000 DOIs obtained from 300 json files from the Crossref database, which can be used for testing and validation purposes.
  
- `output.json`, `affilMatch` and `doisMatch`: The outputs for the `sample.json` file as described above.

- `findOrg.ipynb`: Is another Jupyter Notebook for evaluating the results of the matching algorithm.

- `findYear`: Is a Python script that takes a JSON file as input and generates a CSV file containing the years from the issued date field and the corresponding number of DOIs.

- `description.txt`: Is a description of the main code.


## Dependencies

Make sure you have the following dependencies installed before running the code:

- pandas
- re
- pickle
- unicodedata
- scikit-learn (for `CountVectorizer` and `cosine_similarity`)

## Usage

1. Run the `matching.ipynb` notebook in a Jupyter environment. Make sure to provide the JSON files that you want to match as input.

2. The notebook will process the input JSON files and generate a JSON file with the matchings between DOIs and organization IDs from the OpenAIRE database.


## Contact

If you have any questions, comments, or issues, please feel free to contact me. You can reach me via email at [myrto.kallipoliti@gmail.com]. Feedback and contributions are also welcome.

