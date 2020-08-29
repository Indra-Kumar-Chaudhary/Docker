<h1>Various Commands in Dockerfile</h1>
<b>1. FROM </b>
<p>The FROM keyworkd is used to define the base image, on which we will be building </p>
Example:
FROM ubuntu
<b>2. ADD </b>
<p>The ADD keyword is used to add files to the container being build. The syntax which is followed is <b>ADD <source><destination></b>
Example:
FROM ubuntu 
ADD . /var/wwww/html 

<b>3. RUN</b>
<p>The RUN keyworkd is used to add layers to theh base image, by installing components. 
Each RUN statement adds a new layer to the docker image. 
</p>
<pre>
Example:
FROM ubuntu
RUN apt-get update 
RUN apt-get -y install apache2 
ADD . /var/www/html
</pre>