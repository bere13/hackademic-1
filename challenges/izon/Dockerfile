#Dockerfile to generate an image to this challenge. Download the file and execute the commands at the end to get the chsallenge working
#Install LAMP to the image
FROM tutum/lamp:latest

#get subversion
RUN apt-get -y install subversion

#get files from the challenge
RUN rm -fr /app && svn export https://github.com/bere13/hackademic.git/branches/next/challenges/izon app

EXPOSE 80 3306
CMD ["/run.sh"]


#Once downloaded the file needs to create the image with the following command inside Docker (with dot at the end) : 
#docker build -t nameoftheimage .

#Once created the image to port the challenge to a container/port the following command needs to be executed:
#docker run -d -p 80:80 -p 3306:3306 nameoftheimage

#To find out which IP address has the docker machine: docker-machine ip default
#That IP address needs to be open in the web browser to access to the challenge


