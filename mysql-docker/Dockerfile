FROM mysql 

# Add a database 
ENV MYSQL_DATABASE company 
#add the content of sql-scripts/ directory to your image 
# All scripts in docker-entrypoint-initdb.d/ are automactially 
#executed during container startup 

COPY ./sql-scripts/ /docker-entrypoint-initdb.d/