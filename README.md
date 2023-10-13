# springboot-hello
Publishing a Docker image to Docker Hub using Git, Maven, and Docker involves several steps. Here's a description of the process:

Source Code in Git:
This application's source code is stored in a Git repository. This Git repository can be hosted on platforms like GitHub, GitLab, or Bitbucket. It contains the source code, Dockerfile, Jenkinsfile and any other necessary files for building and packaging your application into a Docker image.

Maven for Build:
Apache Maven is used to build this application. Maven reads the project configuration from a pom.xml file, resolves project dependencies, compiles source code, runs tests, and packages the application into a target binary or JAR file. This build artifact will be used to create a Docker image.

Docker Image Creation:
I have  create a Docker image by defining a Dockerfile, which is a script specifying how the image should be built. The Dockerfile typically includes instructions for copying your application code and its dependencies into the image, setting environment variables, and defining the entry point for the application.  build the Docker image using the docker build command, referencing the Dockerfile.

Docker Image Tagging:
After building the Docker image, I  tag it to specify its repository and version. Tags are used to uniquely identify different versions of the same image. Commonly, images are tagged with a version number, such as myapp:v1.0,I have use latest build as a tag for this application to indicate the image's version.

Docker Hub Account:
To publish  Docker image,we need an account on Docker Hub, a public Docker image registry. I have  create a repository on Docker Hub to store and share  images. (Ensure you are logged in to your Docker Hub account using the docker login command.)

Push to Docker Hub:
To publish  Docker image to Docker Hub, use the docker push command, specifying the image's name and tag. This command pushes the image to  repository on Docker Hub, making it publicly accessible. For example: docker push myusername/myapp:v1.0.

Access on Docker Hub:
Once the image is pushed, it can be accessed and pulled by others. Users can download your image from Docker Hub and run it on their own systems or within their Docker containers.

By combining Git, Maven, and Docker, you have a streamlined workflow for building, packaging, and publishing your application as a Docker image. This allows you to share your application with others and deploy it to various environments with consistency. It's important to ensure that your Docker image is well-documented and that it includes all the necessary dependencies for seamless execution. Additionally, you can automate this process further by integrating it into a CI/CD pipeline to build and publish Docker images automatically whenever code changes are pushed to your Git repository.

Jenkins CI-CD deployment stages:
![image](https://github.com/chintan2812/springboot-hello/assets/142546141/6b65b015-82dc-43be-8f93-2615fd92bf1e)

Console output of jenkins pipeline.
![image](https://github.com/chintan2812/springboot-hello/assets/142546141/92749fca-0ae2-4d20-a640-b9767dc131ef)

Deployment of docker image (on port 8081)
![image](https://github.com/chintan2812/springboot-hello/assets/142546141/22b69d81-fb13-4eac-bc5e-7ffe99de757f)


