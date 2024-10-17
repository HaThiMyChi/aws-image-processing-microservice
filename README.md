# Image Processing Microservice on AWS

Assume you have been hired as a software engineer to develop an application that will help the FBI find missing people.  The application will upload images to the FBI cloud database hosted in AWS. This will allow the FBI to run facial recognition software on the images to detect a match. A NodeJS server is developed and deployed on AWS Elastic Beanstalk. 
A REST API endpoint is implemented in a backend service that processes incoming image URLs.

## Getting Started

You can clone this repo to run the project locally, or test live through Elastic Beanstalk deployment.

## Project Instructions

To complete this project, you will need to:

* Set up node environment
```shell
cd image-processing-microservice
npm i
```

* Run application locally
```shell
npm start
```

* Deploying your system 
```shell
eb init
eb create
eb deploy
```
Check [deployment_screenshot directory](./deployment_screenshot) for deployment output sample


## Testing

* Test the REST endpoint located in the [server.js](./image-processing-microservice/server.js) file
```shell
curl --request GET 'http://image-processing-microservice-dev.us-east-1.elasticbeanstalk.com -?image_url=https://avatars.githubusercontent.com/u/13010388' --output filteredimage.jpg
```
Successful URL responses should have a 200 code. Error codes is returned for the scenario that someone uploads something other than an image and for other common errors.

or

Open in browser:


http://image-processing-microservice-dev.us-east-1.elasticbeanstalk.com/filteredimage?image_url=https://avatars.githubusercontent.com/u/13010388

---

http://image-processing-microservice-dev.us-east-1.elasticbeanstalk.com/filteredimage?image_url=https://images.pexels.com/photos/45201/kitty-cat-kitten-pet-45201.jpeg

