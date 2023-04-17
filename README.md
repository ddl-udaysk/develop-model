# develop-model

Steps/Runbook

1) Add the workflow file present at /.github/workflows/export-model.yml to the model project

2) Create the secrets listed below : <br>
  AWS_ACCESS_KEY_ID -> AWS access key <br>
  AWS_SECRET_ACCESS_KEY -> AWS secret <br>
  CODE -> GITHUB person access token <br>

3) Create the variable listed below : <br>
  MODELNAME -> Model name <br>
  PROJECT_NAME -> Project name in domino <br>
  USER_API_KEY -> Domino User api Key <br>

4) Create a branch of the model project and work on the branch to develop the model in domino using workspaces

5) Merge the branch to the main to start the github actions and the logs should have the api to be used
