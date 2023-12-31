# mlops-with-aws

**1. Basic knowledge about MLOPS & DevOps & SDLC**

**2. AWS basic ( MLOPS tools )**

**3. Linux Basic Commands**

**4. GIT - CodeCommit - Source code Management**

**5. YAML Crash Course**

**6. AWS CodeBuild**
   - start building code build project
   - details about buildspec.yml
   - creating an env variable for a code build project
   - printing default env variable in AWS
   - creating parameters on AWS System Manager > Parameter Store
   - accessing parameter from IAM > code build project roles > create inline policy > to give the permission of GetParameters
   - Save artifacts in S3 bucket
   - Automation of CodeCommit & CodeBuild
   - Amazon EventBridge > rules > event patern / Schedule
   - Event pattern> targeting code build project
   - So if I change anything in my code commit > it will automatically trigger the code build
     
Extra:
 - Learned How to set up a repository with SSH configuration.

**7. AWS CodeDeploy**
  - Two types of deployment. One is **In-Place** and **Blue-Green**
  - Code version > Code Deployment > in to my server
  - Step 1: create ec2 instances to read source code from s3 bucket
  - SSM - Allow deployment group to install/update code deploy agent
  - Step 2: Create application in code deploy
  - Step 3: code revision is pushed to S3
  - Step 4: The deployment group decides which instances to deploy, how to deploy, and which version to deploy
  - Step 5: Deploy the application in Ec2

**8. AWS CodePipeline**
  - each pipeline stage can create Artifacts
  - Artifacts are passed stored in Amazon S3 and passed on to the next stage
  - trigger > CodeCommit > CodeDeploy > Code Repository > deploy

**9. Docker Basic**

**10. AWS SageMaker Basic**
  - Work from the notebook, but not on the notebook
  - Jupyter-friendly env
  - train/deploy easily

**11. AWS SageMaker Basic**
  - Data Collection > Integration > Preparation & Cleaning > Visualization
  - Feature Engineering > Model Training & Hyperparameter tuning > Evaluation > Deployment

**12. AWS SageMaker - Feature Engineering**
  - create S3 bucket > Upload necessary CSV file in S3
  - Open Studio in SageMaker
  - **Data Wrangler Setup**
  - File > New > Data Wrangler Flow > rename the Data Wrangler Flow > Import Data > S3 > Sampling - None ( to import all data ) > click the back button - Data flow
  - Data Flow - Source > Data types > edit ( to edit the data types if needed)
  - **Data Quatlity & Insight Report**
  - data types > + button > data analysis > analysis type - 
  - Target Leakage - we can say which column we have to drop OR which column is less important for prediction
  - **Data Transformation**
  - Data Cleaning/ Pre-Processing based on the Data Quality and Insight Report
  - Balance data || Manage column - drop column || Outliers || Seearch and edit || encode categorcial
  - Custom Data Transformation
  - A Python file (custom-transformer.py
  - **Export S3**
  - Create Job
