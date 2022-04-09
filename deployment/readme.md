# Deploy application for Rocket.Chat with integration of Jitsi

This application knows how to deploy a specific release in the context of Rocket.Chat. 

## Components 

| Name | Version | Image |
|:-------------------|:-------------------------|:------------------------------------|
|rocketchat          |0.1.10-12.20.0-buster-slim|xxx/rocket-chat |
|rocket-jitsi-jicofo |0.1.3-stable-5142         |xxx/jitsi-jicofo|
|rocket-jitsi-jvb    |0.1.3-stable-5142         |xxx/jitsi-jvb   |
|rocket-jitsi-prosody|0.1.3-stable-5142         |xxx/jitsi-prosody|
|rocket-jitsi-web    |0.1.3-stable-5142         |xxx/jitsi-web   |


## Routes:

rocketchat:

| Environment | Internal Route                        | External Route |
|:----------- |:--------------------------------------|:-------------  |
| TEST        | XXXXXX | -              |

jitsi:

| Environment | Internal Route                         | External Route |
|:----------- |:---------------------------------------|:-------------  |
| TEST        | XXXXXX| -              |

## CI/CD
In order to build and deploy a new release, please bump the version in the version's file (./version) and trigger a build on jenkins. After a successful build, a new release is created in octopus and the version is deployed to TEST.

### Build
The project is built on jenkins: <br>

### Deploy
The project is deployed on octopus:<br>

## Host prerequisits

LocalVolumes on Hosts for Mongodb need to be owned by user 1001.

## Data volumes

TEST:

| Host     | Volumes    | Size |
|:---------|:-----------|:-----|
| XXX | mongodb-0  | 30GB |
| XXX | mongodb-1  | 30GB |
| XXX | mongodb-2  | 30GB |  
 

### NFS Backup Share
NFS Backup-Share must contain folder for Backup which is owned by user 1001.

TEST:

| Host                     | Path                               | Size |
|:-------------------------|:-----------------------------------|:-----|
| XXXXX | XXXXX | 20GB |

## Deploy-Application

For more information about the deploy application and it's configuration, please see the section "Deploy-Application" in [cmp-ops-base]

## Build container

```shell
XXXX
``` 

### Run install

```shell
XXXX
```


### Run uninstall

```shell
XXXX
```