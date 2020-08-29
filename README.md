<h1>Various Commands in Dockerfile</h1>
<b>1. FROM </b>
<p>The FROM keyworkd is used to define the base image, on which we will be building </p>
<pre>
Example:
FROM ubuntu
</pre>
<b>2. ADD </b>
<p>The ADD keyword is used to add files to the container being build. The syntax which is followed is <b>ADD <source><destination></b>
</p>
<pre>
Example:
FROM ubuntu 
ADD . /var/wwww/html 
<pre>

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
<b>4. CMD </b>
<p> The CMD keyword is usedto run commands on the start of the container. These commands run only when there is no argument specified while running the container.
</p>
<pre>
Example:
FROM ubuntu 
RUN apt-get update 
RUN apt-get -y install apache2 
ADD . /var/wwww/html
CMD apachectl -D FOREGROUND
</pre>
<b>5. ENTRYPOINT</b>
<p>The ENTRYPOINT keyword is used strictly run commands the moment the container initializes. The difference between CMD and ENTRYPOINT is, ENTRYPOINT will run irrespective of the fact whether orgument is specified or not.
</p>
<pre>
Example:
FROM ubuntu
RUN apt-get update 
RUN apt-get -y install apache2 
ADD . /var/www/html 
ENTRYPOINT apachectl -D FOREGROUND
</pre>

<b>6. ENV </b>
<p>The ENV keyword is used to define environment variables in the container run-time.
</p>
<pre>
FROM ubuntu
RUN apt-get update 
RUN apt-get -y install apache2 
ADD . /var/wwww/html
ENTRYPOINT apachectl -D FOREGROUND 
ENV envariable
</pre>
<p>
So, if there are any environment variables that you want to set inside the container you can pass it using the command env space the name of the variable and space the value of the variable all right so in my case envvariable
</p>