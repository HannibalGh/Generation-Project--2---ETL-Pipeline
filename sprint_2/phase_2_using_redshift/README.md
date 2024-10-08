<h1 align="center"> Where-have-you-Bean </h1>

<p align="center"> Team - Aisha, Hannibal, Rifa, Christina and Ahmed  </p>

---


<h1 align="center"> Contents </h1>


**This folder contains a full set of lambda and IaC files for deploying:**

- Deployment Bucket (**deployment-bucket-stack.yml**)
- Lambda with psycopg2 dependencies bundled with it  AND  Data bucket for CSV files (**cloud_formation.yml**)
- Event trigger for lambda from S3 (**test-lambda.sh**)
- Source folder containing code that will be run by the lambda handler on AWS after the environment has been set up using the above (**src.**)
- A .txt file containing SQL queries used to create our visualizations on Grafana. (**sql_for_grafana.txt**)
- Code walk-through.pdf to explain what is actually occuring (**code walk-through.pdf**)

---


<h1 align="center"> Instructions </h1>


---



## How to - Create and load tables into Redshift database:


Run the **lambda_function.py** file (located in the [src](https://github.com/HannibalGh/Generation-Project--2---ETL-Pipeline/tree/main/sprint_2/phase_2_using_redshift/src) folder).



(As this will also import and run everything in both the **sql_utils.py** and **data_utils.py** files)

---


## Deploying

1) First log into AWS via your VsCode terminal in this folder


2) Then, run the following:

```sh
./install.sh
```

3) Then to trigger the lambda by copying a file to the S3 raw data bucket, run this:

```sh
./test-lambda.sh
```
