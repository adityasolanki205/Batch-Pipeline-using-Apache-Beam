# Batch Processing Pipeline using DataFlow (Under Construction)
This is one of the part of **Introduction to Apache Beam using Python** Repository. Here we will try to learn basics of Apache Beam to create **Batch** pipelines. We will learn step by step how to create a batch pipeline using [German Credit Risk](https://www.kaggle.com/uciml/german-credit). The complete process is divided into 5 parts:

1. **Reading the data**
2. **Parsing the data**
3. **Filtering the data**
4. **Performing Type Convertion**
5. **Data wrangling**
6. **Inserting Data in [Bigquery](https://cloud.google.com/bigquery)**


## Motivation
For the last two years, I have been part of a great learning curve wherein I have upskilled myself to move into a Machine Learning and Cloud Computing. This project was practice project for all the learnings I have had. This is first of the many more to come. 
 

## Libraries/frameworks used

<b>Built with</b>
- [Apache Beam](https://beam.apache.org/documentation/programming-guide/)
- [Anaconda](https://www.anaconda.com/)
- [Python](https://www.python.org/)
- [Google DataFlow](https://cloud.google.com/dataflow)
- [Google Cloud Storage](https://cloud.google.com/storage)

## Code Example

```bash
    # clone this repo:
    git clone https://github.com/adityasolanki205/Batch-Processing-Pipeline-using-DataFlow.git
    
    # Installing Apache Beam on the SDK
    sudo pip3 install apache_beam[gcp]
    
    # Copy the Data from SDK to Cloud Storage
    cd Batch-Processing-Pipeline-using-DataFlow/data
    gsutil cp german.data gs://batch-pipeline-testing/batch/
    
    # Run the Pipeline
    python3 Testing.py --runner DataFlowRunner --project <Your Project Name> --temp_location gs://batch-pipeline-testing/Batch/Temp --staging_location gs://batch-pipeline-testing/Batch/Stage --input gs://batch-pipeline-testing/Batch/german.data --region asia-east1 --job_name germannnalysis
```

## Pipeline Construction

Below are the steps to setup the enviroment and run the codes:

1. **Setup**: First we will have to setup free google cloud account which can be done [here](https://cloud.google.com/free).Then we need to Download the data from [German Credit Risk](https://www.kaggle.com/uciml/german-credit).


    
- **Batch Pipelines**: After learning basics of Apache Beam, let us try to create a Batch Pipeline to run it on Google DataFlow. You can find the repository [Here](https://github.com/adityasolanki205/Batch-Pipeline-using-Apache-Beam.git)

## Credits
1. Akash Nimare's [README.md](https://gist.github.com/akashnimare/7b065c12d9750578de8e705fb4771d2f#file-readme-md)
2. [Apache Beam](https://beam.apache.org/documentation/programming-guide/#triggers)
