

# Learnings:


    1. Minimum qual requirements, and preferred skills are the two most important features to analyze as they provide insights into the job requirements and responsibilities.
    2. The job postings dataset is highly imbalanced, with certain job categories having significantly more job postings than others.
    3. The dataset contains job postings from a diverse range of industries, including healthcare, logistics, manufacturing, education, finance, and technology.
    4. The total number of dataset is 2,947 job postings 
    5. The dataset can help identify the most popular Business titles, recruiting agency with the most job postings, and the most sought-after or preferred skills and academic qualifications.


# Challenges:

    1. The dataset does not provide information about the candidates who applied for the jobs, which could limit the ability to understand the job market from a job seeker's perspective.
    2.  The dataset only covers a limited time period (between 2011 and 2019). Hence, the job market in New York City may have changed  significantly since then.
    3.  Data quality issues, such as missing values or inconsistent formatting, could impact the accuracy of the analysis. Hence, data cleaning and preprocessing, checking for duplicates or errors, and dealing with missing values should be done for accurate data insights.
    4.  Dealing with outliers, such as extremely high or low salaries, which could skew the analysis.
    5.  The salary information in the dataset may not be accurate, as it is often listed as a range and may not reflect the actual salary offered.


# Considerations:
      
    1.  Data collection method: Was the data collected through surveys, job postings, or administrative records? This can affect the representativeness of the dataset.
    2.  Data quality: How complete and accurate is the data? Are there missing values, outliers, or errors that need to be addressed?
    Variables included: What variables are included in the dataset, and do they accurately reflect the job market in New York City? The dataset contains information on job postings, not necessarily on job hires, which means that some job postings may not have resulted in a hire.
    3.  Timeframe: What time period does the data cover, and is it up-to-date and relevant to current labor market conditions?
        The dataset contains information only for the year between 2011 and 2019, and may not be representative of the job market in other years.

    4.  Bias: Is the dataset representative of the diversity of New York City's job market, or does it have any biases or limitations in its coverage?


# Assumptions:

    1.  The job postings are a accurate reflection and representative of the actual job responsibilities of the job market demand in New York City, with minimal errors or omissions.
    2.  The variables included in the dataset are relevant and informative for understanding the job market in New York City.
    3.  There are no significant biases in the data collection or reporting that would skew the results.
    4.  The salary ranges provided in the dataset are a good approximation of the actual salary offered.


**If any deployment to be done, proposals of the deployment steps**

# Deploy the Jupyter Notebook (.ipynb) file to Amazon (AWS) SageMaker


    1.  Create an S3 bucket for storing the "nyc-jobs.csv" dataset and "assesment_notebook.ipynb" files.

    2.  Upload the files to the S3 bucket you created in the first step.

    3.  Open the AWS SageMaker Console and select "Notebook instances". Click on "Create notebook instance" and enter an instance name, pick the right family,  size, version, elastic inference, EBS volume (maximum size is 15G). Select an appropriate instance type and then choose the network VPC and subnet. Under "Permissions and encryption", create or select an IAM role that has the necessary permissions to access the S3 bucket where your Jupyter Notebook file is stored. Click on "Create notebook instance" to create your instance. Once your instance is created, click on "Open JupyterLab" to launch JupyterLab in your browser.

    4. In JupyterLab, navigate to the folder where your Jupyter Notebook file is stored. Click on "Upload" in the JupyterLab interface and select your Jupyter Notebook file (.ipynb) from S3 bucket. Once your file is uploaded, you can open it in JupyterLab and start working on it

    5.  Create an Amazon SageMaker endpoint configuration that specifies the type of instance to use, the number of instances, and any other configuration details. 

    6.  Run the SageMaker notebook instance and start executing cells to see the output

    7.  Monitor and maintain your deployment: This involves monitoring metrics such as accuracy, latency, and throughput, and making any necessary adjustments to the deployed file to improve performance. Switch off your instance when done to avoid cost.

  

# If you had to trigger your code, please suggest your approach.

    1.  Open the AWS Management Console and navigate to the SageMaker. Click on the "Notebook instances" link in the left-hand navigation pane.
    2.  Find the notebook instance that you want to use and click on the "Open JupyterLab" button next to it. Once JupyterLab is open, navigate to the directory where your .ipynb file is located.
    3.  Click on the "assesment_notebook.ipynb" file to open it. If the notebook has not already been run, click on the "Run" button to execute each cell of the notebook.