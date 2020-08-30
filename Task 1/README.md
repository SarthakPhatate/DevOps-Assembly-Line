# DevOps
## Website Automation Using jenkins and docker

### Step 1: Setup job1 
<p>1. This job will check whether an push is made on master branch with help of git poll scm<p>
2. If commit is made then it will automatically be triggered and the updated content is copied to webmaster folder and docker container is ran 
<p>3. Thus the website is up<p>

![Step 1](https://raw.githubusercontent.com/SarthakPhatate/DevOps-Assembly-Line/master/Task%201/images/1.png)

The website is as follow
![Step 2](https://raw.githubusercontent.com/SarthakPhatate/DevOps-Assembly-Line/master/Task%201/images/2.png)

### Step 2: Setup job2
<p>1. This job will check whether an push is made to dev1 branch with help og git poll scm<p>
<p>2. If push is made then it will automatically be triggered and the updated content is copied to webdev folder and docker container is ran
<p>3. Thus the website is up<p>
  
![Step 2](https://raw.githubusercontent.com/SarthakPhatate/DevOps-Assembly-Line/master/Task%201/images/3.png)
  
The website is as follow
![Step 2](https://raw.githubusercontent.com/SarthakPhatate/DevOps-Assembly-Line/master/Task%201/images/5.png)

### Step 3 : Setup job 3
<p>1. This job is for operational team which check the dev1 website changes and if prefect running then<p>
<p>2. Runs this commad curl --user "admin:********" http://289e4de0.ngrok.io/job/job3/build?token=devops<p>
<p>3. Thus the job3 gets triggered content of dev1 branch is merged to master brnch and main website is updated as below<p>
  
The website is as follow
![Step 2](https://raw.githubusercontent.com/SarthakPhatate/DevOps-Assembly-Line/master/Task%201/images/8.png)
