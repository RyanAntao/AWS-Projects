# To the power of math

To the power of math! Is an AWS web application that takes the base number, power number and gives the value.

Services used: AWS Amplify, AWS Lambda, Amazon API Gateway, Amazon DynamoDB and AWS IAM

Steps: 
* Download the project files
* Head to the AWS management console and open AWS Amplify 
* Create new app and and then Host web app
* Now select Deploy without Git provider 
* Give the App name PowerOfMath and drag and drop the index file(zipped). Save and deploy
![Screenshot 2024-06-30 172606](https://github.com/RyanAntao/AWS-Projects/assets/101993568/eeab7f3c-16a3-414e-b672-569ed38f516c)
* You will now get the domain link
* Head to the AWS management console and open Lambda
* Create a function. Name it PowerOfMathFunction. Select the latest version of python for runtime.
* For code source use the code given in the lambda file. Save and deploy
![Screenshot 2024-06-30 172811](https://github.com/RyanAntao/AWS-Projects/assets/101993568/69c828c0-9aa4-4f64-901e-f6627a278d68)
![Screenshot 2024-06-30 172850](https://github.com/RyanAntao/AWS-Projects/assets/101993568/f92bf3d9-3b59-44d1-839c-ed0a00666385)
* Head to the AWS management console and open API Gateway 
* Create API and then build REST API. Name it PowerOfMathAPI
* Under resources create a method the type of method will be POST. Select the lambda function as PowerOfMathFunction. Save.
![Screenshot 2024-06-30 173225](https://github.com/RyanAntao/AWS-Projects/assets/101993568/4d012919-5675-4944-899f-6159d2c71ff4)
* Now, enable CORS. Click on Enable CORS and replace CORS headers
* Deploy API and set the deployment stage as new stage. Enter stage name as dev and then deploy 
* Copy the Invoke URL and save it.
* Head to the AWS management console and open DynamoDB 
* Create table. Give the table name PowerOfMathDatabase. For partition key enter ID
![Screenshot 2024-06-30 173313](https://github.com/RyanAntao/AWS-Projects/assets/101993568/45328fe4-e609-4194-9f95-714dffae6848)
* Now open the table, under General Information click on additional info and save the ARN
* Now go to lambda under permissions go to configuration and click on the role name link
* Add permissions and create inline policy 
* In the json tab replace the code with the json code from the project files
* In the json code in resource replace it with your table ARN and click on review policy and give it the name PowerOfMathDynamoPolicy and create policy 
* Your AWS web application is now ready to use! (On the domain link)
![Screenshot 2024-06-30 173332](https://github.com/RyanAntao/AWS-Projects/assets/101993568/b46533cb-0777-4fab-84d6-0d90fe6f6b64)
![Screenshot 2024-06-30 173342](https://github.com/RyanAntao/AWS-Projects/assets/101993568/fcdf2f96-91cd-40d4-a724-09b850c5f5b5)


