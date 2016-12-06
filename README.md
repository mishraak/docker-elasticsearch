# Elasticsearch

This is a custom image for ES I'm using for my docker-elk project. 
We are mostly default ES except a couple of tweaks to enable CORS on ES so as to make ajax calls from our web page successfully.
Even though this image is built to ideally run in conjunction with other two images but you may edit and use it by updating config and creating a separate image.

## Getting Started

There are two ways to use this image.
1. Simply build the image using given Dockerfile and config file using docker build command as follows. 
   Clone the repository to your machine and cd into it.

```	
docker build -t <name of your choice> .
```	

2. For this to work, download Elasticsearch, Logstash and docker-elk-ui images to your machine inside a folder let's say docker-elk.
   	Now cd to that folder and this image (and other) will be built from scratch automatically when you fire coomand as below :

   	```
	docker-compose up --build
	```

### Prerequisites

What things you need to install the software and how to install them

You need to install docker and docker-compose (optional if you plan to run only ES).
Please use latest versions for both as some of the commands may not work in older versions.


## Running the test 
If you have spun up only ES container, then you can test it by 
1. First run below command to see if ES container is running.	
		
```
docker ps
```

Now open below URL in any browser and see if ES is running fine. http://127.0.0.1:9200/
If it returns a valid json response, it means ES is running just fine.

If you have spun up all (E,L,K) containers instead of just one, you can open below URL and check if you see any graphs: 

http://127.0.0.1/responseplot.html 	or	http://127.0.0.1/urlplot.html 



## Deployment

You can deploy this on any cloud env that supports docker containers like Amazon EC2 etc.



## Authors

* **Akshay Mishra** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)
