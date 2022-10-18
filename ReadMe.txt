< <<<< https://github.com/Sakshi-25/PostmanTesting/blob/main/README.md >>>>>>>>

Starting with POSTMAN + Github API
Step1: Account on Github -> Settings -> Developer Settings -> Personal Access Tokens -> Generate New Token copy it

-- Step 2: Download & Install Postman. Login with Google or anything and Open it.

Create a Workspace
Create a Request
Go to Envinronment Variable on top-right corner & click on settings(Manage Environment)
Add / Creare an environment

Name the environment : Github API

variable	Initial	Current
token	Leave it empty	Paste Your github access token here
Update

Choose the environment
Create a new request
Environment Setup is done.

-- Step3: Now, Make a Request.

POSTarrow_down_small	https://api.github.com/user/repos
POST means we are creating a new repo.	POST /user/repos
Details
Details
Choose Body

Select raw & JSON & paste this example data. Change the repository name and description as per your choice. This Repo will be Public as private = false

{
  "name": "Hello-World",
  "description": "This is your first repository",
  "homepage": "https://github.com",
  "private": false,
  "has_issues": true,
  "has_projects": true,
  "has_wiki": true
}
Send
Status: Error 401 Authorization Error(Unauthorised)
To Enable Authorization: Go to Authorization -> Type -> Bearer Token (As we have token)-> Put the token as {{token}} (safe way to use token)
Send
Status: OK 201 Created
confetti_ballsparkles A repository has been created on your github accountdesktop_computer
