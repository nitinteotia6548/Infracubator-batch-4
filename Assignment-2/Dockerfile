FROM golang:latest
#Set the working directory inside the container
WORKDIR /app
#Copy the application source code from this go-app folder into the container
COPY go-app /app/
#Generate binary file of go-app
RUN make build
#Expose the go application on local port 8080
EXPOSE 8080
#Run generated binary file
CMD ["./out/go-app"]
