# Title

## Building the Web site Docker image

The image currently needs to be manually built locally and then pushed to Docker Hub. The image is built and pushed with a tag of `latest`.

First log in to Docker:

```bash
docker login -u yourusername
[enter your password]
```

Then build and push the image:

```bash
docker build --tag stevejay/ons-exploreratest --file Dockerfile .
docker push stevejay/ons-exploreratest
```

### Building and running locally

If you want to test building and running the image locally, then run the following command from the project root: `docker-compose up --force-recreate --build --detach`. You should now be able to access the Web site at `http://localhost:6008/`.
