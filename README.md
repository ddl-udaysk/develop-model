# Develop Model Runbook

Steps/Runbook

1) Add the workflow file present at /.github/workflows/export-model.yml to the model project. The workflow uses the scripts from the repo    https://github.com/ddl-udaysk/domino-sagemaker-github-actions

2) Create the secrets listed below : <br>
  AWS_ACCESS_KEY_ID -> AWS access key <br>
  AWS_SECRET_ACCESS_KEY -> AWS secret <br>
  CODE -> GITHUB person access token <br>
![Screen Shot 2023-04-17 at 1 48 57 PM](https://user-images.githubusercontent.com/97467901/232568338-d6d001bc-7eed-429e-98c7-eb105c09b962.png)

3) Create the variable listed below : <br>
  MODELNAME -> Model name <br>
  PROJECT_NAME -> Project name in domino <br>
  USER_API_KEY -> Domino User api Key <br>
  ![Screen Shot 2023-04-17 at 1 49 16 PM](https://user-images.githubusercontent.com/97467901/232568414-1f0193c8-b8e0-4c0e-9d69-7af3a6650678.png)


4) Create a branch of the model project and work on the branch to develop the model in domino using workspaces

5) Merge the branch to the main to start the github actions and the logs should have the api to be used. You can test the endpoint using Curl as show below:<br>
   curl https://r039xwjush.execute-api.us-west-2.amazonaws.com/api/api -H 'Content-Type: application/json' -d '{"data": {"start": 1, "stop": 100}}'
<br>
   Please note that we need to /api to the endpoint that we get from the logs.
<br>
 ![Screen Shot 2023-04-17 at 1 46 49 PM](https://user-images.githubusercontent.com/97467901/232567938-30212e57-9562-49cd-b44b-4db67d0b9f87.png)
![Screen Shot 2023-04-17 at 1 48 05 PM](https://user-images.githubusercontent.com/97467901/232568169-4c36be19-c9c8-415c-8f07-ba99da2e14a2.png)
