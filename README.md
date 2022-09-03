# Overview

This project illustrates how to deploy a machine learning python application using the concepts of CI/CD. Therefore, Azure App Services and Azure Pipelines are used.

## Project Plan

* A link to a Trello board for the project: https://trello.com/invite/b/dWyJ3CJH/72ed2d745b210faee010f64f3fc4e010/pipelineproject
The board is definitely set to public. In case it does not work again - here is a screenshot:

<img width="865" alt="Bildschirmfoto 2022-09-01 um 21 06 18" src="https://user-images.githubusercontent.com/25867675/187993244-c37db987-569f-420a-9184-92e8a149925c.png">

* The spreadsheet is uploaded as Excel file document in the GitHub repository (called "Plan.xlsx")

## Instructions

* Architectural Diagram (Shows how key parts of the system work)

![PipelineProject](https://user-images.githubusercontent.com/25867675/186108902-7f148f24-51ed-4b73-8e0b-fc1e82764aa9.jpeg)

Below are instructions for running the Python project.

* Project cloned into Azure Cloud Shell by creating ssh-keys ("ssh-keygen -t rsa"), getting public key (“cat /home/odl_user/.ssh/id_rsa.pub” and copy the key into to GitHub. Then clone repo to Azure by using "git clone sshCodeFromGitHub” (https://user-images.githubusercontent.com/25867675/186249179-afb688b3-3b67-4aa4-9915-d4acf9001f70.png)

<img width="888" alt="Project_cloned_to_Azure" src="https://user-images.githubusercontent.com/25867675/186111763-a542f7af-d7de-4ec5-a651-b85b8f669aea.png">


* Checking if tests are passed after running the "make all" command from the Makefile

<img width="1435" alt="Makefile_test_passed_2" src="https://user-images.githubusercontent.com/25867675/186249445-f03a325b-6627-4225-83fa-da8c3b85e909.png">


* Output of a test run using GitHub Actions as build server

<img width="1433" alt="GitHub_Actions_passed" src="https://user-images.githubusercontent.com/25867675/186250428-851cdde0-3cdc-4dc1-a24b-8e25ec48a24d.png">

<img width="1426" alt="GitHub_Actions_passed_2" src="https://user-images.githubusercontent.com/25867675/186250467-b3cca8ad-b6b8-4c85-b644-bdd034e2edb7.png">

<img width="1414" alt="GitHub_Actions_Badge_ReadMe" src="https://user-images.githubusercontent.com/25867675/186251035-6166c9b7-fffd-4438-ba82-386cac2e7de1.png">

* Successful deploy of the project in Azure Pipelines and automatic deployment of Azure App Service from Azure Pipelines

<img width="1225" alt="Pipeline successfully working" src="https://user-images.githubusercontent.com/25867675/186251760-5b185873-54db-4aa4-ab76-bdd6a1df1049.png">

* Successful prediction from deployed flask app in Azure Cloud Shell.

<img width="813" alt="website_running" src="https://user-images.githubusercontent.com/25867675/186251949-9e56f491-9489-40ad-a0b4-c08d8a44fedd.png">

The output of the working application (please note the name is different as I had to re-run this step several times as there was a mistake in the code provided by Udacity)

<img width="643" alt="Bildschirmfoto 2022-08-31 um 10 38 13" src="https://user-images.githubusercontent.com/25867675/187635498-8ac084bc-d1a1-4e4c-a9ee-d6ce3c04cd0d.png">


* Output of streamed log files from deployed application

<img width="1229" alt="Log Files" src="https://user-images.githubusercontent.com/25867675/186251222-dc73f788-fcf9-4f48-be29-4d880a7400a2.png">

* Locust test screenshot

<img width="1233" alt="Locust_screenshot" src="https://user-images.githubusercontent.com/25867675/187927476-42cb26da-fd52-403c-beeb-07bec6907fdf.png">


## Enhancements

The project can be improved. One idea would be to include alerts, for example when the web server fails. Once the project scales and multiple steps are required within the ML application it would be wise to include an effective microservice strategy including a production and a stage environment as well as load balancing.

## Demo 

Here is a link to a demo: https://youtu.be/h_e0M2jSXPA.
Here is a link to a live demo demonstrating the functioning of the pipeline: https://youtu.be/Js8k-DUkgwc

