# Meme matching game
Meme matching game is a game that uses continuous deployment pipeline from GitHub to S3

Services used: Amazon S3, CodePipeline and Github

Steps:
* Download and upload all the files to your GitHub 
* Head to the AWS management console and open S3
* Create a bucket and name it my-meme-game and deselect the option Block all public access
![Screenshot 2024-07-01 004927](https://github.com/RyanAntao/AWS-Projects/assets/101993568/8ccd0b13-51a8-4511-bacd-0fcdf58de5eb)
* Open the bucket and go to properties and enable static website hosting, specify the index document as index.html and save
![Screenshot 2024-07-01 004951](https://github.com/RyanAntao/AWS-Projects/assets/101993568/a1a710b8-4cab-470c-8dcc-3a463dce2df7)
* Open bucket permissions and edit bucket policy and paste the given bucket policy then update your bucket name 
* Head to the AWS management console and open CodePipeline 
* Create pipeline, name it meme-pipeline and click next
![Screenshot 2024-07-01 005104](https://github.com/RyanAntao/AWS-Projects/assets/101993568/83811ed1-8614-4dc7-bf2b-b9019edce4a2)
* For source provided select GitHub version 2, click on connect to GitHub, for connection name enter meme-github-pipeline and connect to GitHub, click on install a new app and select the the only select option and click on your repository, save it and click connect
![Screenshot 2024-07-01 003127](https://github.com/RyanAntao/AWS-Projects/assets/101993568/792404a6-4b57-4d14-a4de-ff62c9754172)
* For connection select meme-github-pipeline then select your repository name
* For pipeline trigger select push in branch and select CodePipeline default and click next
![Screenshot 2024-07-01 003440](https://github.com/RyanAntao/AWS-Projects/assets/101993568/56e7a6eb-7303-486b-9946-69bea7e8af79)
* Skip build stage
* For deploy stage select Amazon S3 and select your bucket name 
* Check the checkbox that says extract file before deploy and click next
* Review everything and create pipeline
![Screenshot 2024-07-01 004310](https://github.com/RyanAntao/AWS-Projects/assets/101993568/aaaffb2c-d7a7-4115-83bd-6f77d47ef1f3)
![Screenshot 2024-07-01 004320](https://github.com/RyanAntao/AWS-Projects/assets/101993568/6c270809-23f5-4f29-b25a-08375616cc90)
![Screenshot 2024-07-01 004329](https://github.com/RyanAntao/AWS-Projects/assets/101993568/3234eff4-f17f-49de-9470-6d767e0a2377)
![Screenshot_1-7-2024_04617_ap-south-1 console aws amazon com](https://github.com/RyanAntao/AWS-Projects/assets/101993568/aa666e10-e11a-4133-bad2-e536bac1422d)
* Use the static website hosting link of your bucket to open your game
![Screenshot 2024-07-01 004951](https://github.com/RyanAntao/AWS-Projects/assets/101993568/24d51fb3-8229-46a1-95e8-607a35df7e23)
![Screenshot 2024-07-01 004710](https://github.com/RyanAntao/AWS-Projects/assets/101993568/c84dfde5-66a9-4feb-ac29-3a7604fb4b61)
![Screenshot 2024-07-01 004728](https://github.com/RyanAntao/AWS-Projects/assets/101993568/586c1498-7ef6-4a12-b2b3-6fb50f546677)
![Screenshot 2024-07-01 004748](https://github.com/RyanAntao/AWS-Projects/assets/101993568/937618d2-cddc-4260-b4be-a03defd5271d)
* Any changes made in the GitHub files will update the game
