# Welcome to Matrix

[![Maintainability](https://api.codeclimate.com/v1/badges/a41e6e73f69c94d8b9c5/maintainability)](https://codeclimate.com/github/ResultadosDigitais/matrix/maintainability) [![CircleCI](https://circleci.com/gh/ResultadosDigitais/matrix.svg?style=svg)](https://circleci.com/gh/ResultadosDigitais/matrix)

## What's Matrix

The objective of **#matrix** project is to offer a virtual environment office, as nice as fisical offices. When we are working in a fisical office is very common entering in discussion threads in many diferents environments, for example: On coffe, On lunch and others.

When we are working remotely there are no conversations like in a fisical office. The **#matrix** project was born as a proposal to better that experience. The idea is to create a lot of virtual rooms where people can see and enter these rooms to participate.

**#matrix** produces a virtual office for remote teams. In this project, you can run a virtual office to simulate the physical environment. Read more [here](https://medium.com/rd-shipit/matrix-d4cfc4ad4c75)

## login Page
The login is so simple. You only need to create a google client id and configure the environment variable GOOGLE_CREDENTIAL=xxxxxxxxxxx.apps.googleusercontent.com. Follow [this step by step](/docs/GOOGLE-CREDENTIAL-STEP-BY-STEP.md) to configure your own google client key.

![Login Page](docs/img/matrix-login.png)

## The rooms Inside of #matrix
 
The inside of **#matrix** there are some rooms. In this rooms is possible to see others colleagues and if they are talking or in a meeting in the avatar will apear a head set icon. (eg. In the image the guys in the Platform-Email romm are in a meeting)  

![Matrix Room](/docs/img/matrix-rooms.png)

![Matrix Online](/docs/img/matrix-online.png)

## The meeting window

You can only enter in a room to show for the other that you are avaliable there through the `ENTER ROOM` button or enter in a meeting through the button `ENTER MEETING`. 

![Matrix Meet](/docs/img/matrix-meet-room.png)


## Getting Started

If you want run the **#matrix**, you need follow steps:

1. We are using Google to authorizations, you need create a credential [here](/docs/GOOGLE-CREDENTIAL-STEP-BY-STEP.md) you can follow step by step

2. Run appplication with docker compose:

		$ docker-compose up

3. Open your brownser and access: 

		http://localhost:8080/

4. When you finish, you can run:

		$ docker-compose down
		
# On Heroku
If you prefer, you can run **#matrix** in Heroku: 

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/ResultadosDigitais/matrix)

# On GCP 
If you prefer, you can run **#matrix** in GCP:

[![Run on Google Cloud](https://deploy.cloud.run/button.svg)](https://deploy.cloud.run?git_repo=https://github.com/ResultadosDigitais/matrix&revision=add-gcp-button)


## Environments

The **#matrix** project has some environments that important to define.

1. We are using Google to authorizations, you need create a credential [here](https://developers.google.com/identity/sign-in/web/sign-in) and before define this:

		GOOGLE_CREDENTIAL=${paste_your_credention_here}

2. If you are running with ssl It's important to configure SSL, to define this:

		ENFORCE_SSL=true

3. The Matrix needs to know, where it get rooms definitions:

		ROOMS_SOURCE=ENVIRONMENT

4. There is a config that define the rooms of The **#matrix**, if you prefer you can generate the unique id per room [here](https://www.uuidgenerator.net), to define this:


		ROOMS_DATA=[
		   {
		      "id":"${UUID}",
		      "name":"Lounge",
		      "disableMeeting":true
		   },
		   {
		      "id":"${UUID}",
		      "name":"WAR ROOM CDP"
		   },
		   {
		      "id":"${UUID}",
		      "name":"Data Services"
		   }
		 ]


## Contributing
We encourage you to contribute to The **#matrix**!

Everyone interacting in **#matrix** codebase, issue trackers, chat rooms, and mailing lists is expected to follow [code of conduct](docs/CODE_OF_CONDUCT.md).


## License
The **#matrix** is released under the [MIT License](docs/LICENSE)



`"The answer is out there, Neo, and it's looking for you, and it will find you if you want it to."`
