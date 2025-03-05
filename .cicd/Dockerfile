# Instrustions

#This is the official image as a base
FROM openjdk:18

#Create a directory called /opt/i27 in which we store our artifacts and other read only data.
RUN mkdir -p /opt/i27/

#Setting the work directory to /opt/i27
WORKDIR /opt/i27

#Define a buildtime variable called JAR_SOURCE to specify the path format
ARG JAR_SOURCE

COPY ["${JAR_SOURCE}", "/opt/i27/i27-users.jar"]

#Grant executable permissions to the workdir
RUN chmod 777 /opt/i27/

#Expose Port 8761 to allow access to application
EXPOSE 8232

#Run the process
CMD ["java", "-jar", "/opt/i27/i27-users.jar"]