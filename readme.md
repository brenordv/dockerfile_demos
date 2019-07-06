# Dockerfile examples
This repo has a couple of examples of Dockerfile + docker-compose.yml to create an image using the files from my dummy-api repository.


## git_image
This will clone a repository and create an image using it's files.


## local_image
Will copy local files to create the image. To use this, first you have to clone the repository inside the local_image folder.

```shell
cd local_image
git clone https://github.com/brenordv/dummy-api.git
```

## Building the images

To build any of the images, access one of the folders (git_image or local_image) and use one of the commands:

```docker
docker-compose up -d
```

or

```docker
docker build -t my_image_name:image_tag .
```

