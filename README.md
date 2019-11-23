Docker Google Cloud SDK
====

This is a docker image source for [Google Cloud SDK](https://cloud.google.com/sdk/docs/?hl=ja)

## Description
- SDK: [Docker Cloud SDK](https://hub.docker.com/r/google/cloud-sdk/)

## Install
```
$ docker pull ukitomato/google-cloud-sdk
$ docker run -ti --name gcloud-config ukitomato/google-cloud-sdk auth login
```

## Usage
1. add .bash_profile
```
alias gcloud='docker run --rm -ti --volumes-from gcloud-config -v $(pwd):/working -w /working ukitomato/google-cloud-sdk'
```
2. you can use gcloud commands as if it were installed locally
```
$ gcloud version
```

## Licence

[MIT](https://github.com/ukitomato/docker-google-cloud-sdk/blob/master/LICENSE)

## Author
Yuki Yamato [[ukitomato](https://github.com/ukitomato)]
