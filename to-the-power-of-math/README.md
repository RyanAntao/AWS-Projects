# To the power of math

To the power of math! Is an AWS web application that takes the base number, power number and gives the value.

Services used: AWS Amplify, AWS Lambda, Amazon API Gateway, Amazon DynamoDB and AWS IAM

Steps: 
* Download the project files
* Head to the AWS management console and open AWS Amplify 
* Create new app and and then Host web app
* Now select Deploy without Git provider 
* Give the App name PowerOfMath and drag and drop the index file(zipped). Save and deploy 
* You will now get the domain link
* Head to the AWS management console and open Lambda
* Create a function. Name it PowerOfMathFunction. Select the latest version of python for runtime.
* For code source use the code given in the lambda file. Save and deploy 
* Head to the AWS management console and open API Gateway 
* Create API and then build REST API. Name it PowerOfMathAPI
* Under resources create a method the type of method will be POST. Select the lambda function as PowerOfMathFunction. Save.
* Now, enable CORS. Click on Enable CORS and replace CORS headers
* Deploy API and set the deployment stage as new stage. Enter stage name as dev and then deploy 
* Copy the Invoke URL and save it.
* Head to the AWS management console and open DynamoDB 
* Create table. Give the table name PowerOfMathDatabase. For partition key enter ID
* Now open the table, under General Information click on additional info and save the ARN
* Now go to lambda under permissions go to configuration and click on the role name link
* Add permissions and create inline policy 
* In the json tab replace the code with the json code from the project files
* In the json code in resource replace it with your table ARN and click on review policy and give it the name PowerOfMathDynamoPolicy and create policy 
* Your AWS web application is now ready to use! (On the domain link)
