[comment]: <> (# Rasa NLU server template)

[comment]: <> ([comment]: <> &#40;This template contains all you need to deploy [Rasa NLU]&#40;https://rasa.com/&#41; server on [Heroku cloud]&#40;https://heroku.com&#41; to make your Rasa project visible globally.&#41;)

[comment]: <> ([comment]: <> &#40;## How to use&#41;)

[comment]: <> (Click on the button below to deploy this template on your Heroku instance.)

[comment]: <> (Heroku will automatically build the Docker image and your project's NLU model.)

[comment]: <> ([![Deploy to Heroku]&#40;https://www.herokucdn.com/deploy/button.svg&#41;]&#40;https://heroku.com/deploy&#41;)

[comment]: <> (_It takes a couple of minutes to build and start the server. You can see the progress in Heroku logs._)

[comment]: <> (## How to make requests)

[comment]: <> (Once your server is deployed, you can make requests to your NLU model via [Rasa HTTP API]&#40;https://rasa.com/docs/rasa/api/http-api/#operation/parseModelMessage&#41;)

[comment]: <> (For example:)

[comment]: <> (`curl https://<your Heroku application name>.herokuapp.com/model/parse -d '{"text":"hello"}'`)

[comment]: <> (## How to change the model)

[comment]: <> (Once you've deployed and tested your NLU server, you can then clone it to your machine and make changes in NLU model.)

[comment]: <> (### 1. Clone the application)

[comment]: <> (Install [git]&#40;https://git-scm.com/downloads&#41; and [Heroku CLI]&#40;https://devcenter.heroku.com/articles/heroku-cli#download-and-install&#41;.)

[comment]: <> (Run a terminal &#40;or console&#41; on your machine and type)

[comment]: <> (```)

[comment]: <> (heroku login)

[comment]: <> (heroku git:clone -a <your Heroku application name>)

[comment]: <> (cd <your Heroku application name>)

[comment]: <> (git remote add origin https://github.com/just-ai/rasa-heroku-template)

[comment]: <> (git pull origin master)

[comment]: <> (```)

[comment]: <> (_You have to do these steps only once per project._)

[comment]: <> (### 2. Make changes)

[comment]: <> (#### Install Rasa)

[comment]: <> (Install Rasa on your machine. Here is a great [installation guide]&#40;https://rasa.com/docs/rasa/user-guide/installation/&#41;.)

[comment]: <> (#### Train NLU model)

[comment]: <> (Then go to the directory of your application &#40;cloned on the previous step&#41; and make some changes in the model.)

[comment]: <> (Please refer to the [Rasa documentaion]&#40;https://rasa.com/docs/rasa/user-guide/rasa-tutorial/&#41; to learn how to build and evaluate NLU model.)

[comment]: <> (> Please note that you don't have to run **rasa init** command once your template project is already cloned from Heroku.)

[comment]: <> (Also note that NLU server doesn't run any actions - it only runs your NLU model. Thus you can use only **rasa train nlu** command.)

[comment]: <> (#### Evaluate changes)

[comment]: <> (To evaluate your changes on your local machine just run NLU server locally and make some HTTP requests to the [Rasa HTTP API endpoint]&#40;https://rasa.com/docs/rasa/http-api&#41;.)

[comment]: <> (You can also use [shell command]&#40;https://rasa.com/docs/rasa/command-line-interface#rasa-shell&#41; to try your mddel without running a server.)

[comment]: <> (#### Push changes to Heroku)

[comment]: <> (Once you've trained and evaluated your NLU model, you can push changes to Heroku.)

[comment]: <> (Run the next commands in the terminal)

[comment]: <> (```)

[comment]: <> (git add .)

[comment]: <> (git commit -am "some comments")

[comment]: <> (git push)

[comment]: <> (```)

[comment]: <> (Heroku will automatically handle the changes, re-build NLU model and re-start the server.)

[comment]: <> (> Please note that locally trained NLU models won't be pushed to the Heroku repository.)
