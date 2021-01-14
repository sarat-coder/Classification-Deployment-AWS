# Classification-Deployment-AWS
Dog Cat Classification Deployment

# Steps we are following to deploy our app on AWS Elastic BeanStalk

    Step1: Your main python file name should be application.py (easy way to double click on object name right click and click on refactor and rename to application)
    Step2: Your flask object name, which we have defined in application.py should also be the application.
    Step3: .ebignore  is responsible to hold the name of those files which we don't want to push on a cloud.
		(right click on project , create new file)
    Step4: Create a requirements.txt file
            command : pip freeze > requirements.txt
    Step5: Create a folder in your application and name it as .ebextensions
		(right click on plroject, create new directory)
    Step6: Inside .ebextensions we have to create a new file and name it as python.config
		(right clink on .ebextensions, create a new file and named it as python.config)
    Step7: In python.config we are suppose to mention the below commands
             option_settings:
                  "aws:elasticbeanstalk:container:python":
                    WSGIPath: application:application

    Step8: Those files we need to push to cloud need to select them in the folder and zip them FILE NAME SHOULD BE WITH EXTENSION .ZIP
Go to AWS page
Search for Elastic Beanstalk=> create a new application
PUT THE NAME OF APPLICATION
NEXT MENTION PLATFORM AS PYTHON
aPPLICATION CODE USE :- UPLOAD YOUR CODE OPTION

link:-http://dogcatclassifier-env.eba-36e8d2zm.us-east-2.elasticbeanstalk.com/
