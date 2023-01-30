# dotnet7 Development Container

## Quickstart

Build the docker image containing the base images for the apsnet 7.0 runtime and the 7.0 sdk from Microsoft's docker hub 

docker build -t dotnet7-sample:dev --target dev .

docker run -it -v ${PWD}:/work dotnet7-sample:dev bash